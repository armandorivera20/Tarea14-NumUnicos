# Tarea14-NumUnicos
    def eliminar_duplicados(nums):
    # Verificar si el arreglo está vacío
    if len(nums) == 0:
        return 0
    
    # Inicializar el contador de elementos únicos y el índice de elementos únicos
    k = 1
    indice_unico = 0
    
    # Recorrer el arreglo desde el segundo elemento
    for i in range(1, len(nums)):
        if nums[i] != nums[indice_unico]:
            indice_unico += 1
            nums[indice_unico] = nums[i]  # Mover el elemento único a la posición correspondiente
            k += 1  # Incrementar el contador de elementos únicos
    
    # Regresar el número de elementos únicos
    return k

    # Ejemplo de uso
    nums = [1, 1, 2, 2, 3, 4, 4, 5, 16, 70, 70]
    k = eliminar_duplicados(nums)
    print(f"Número de elementos únicos: {k}")
    print(f"Arreglo modificado (primeros {k} elementos únicos): {nums[:k]}")

# potencia-SR
def potencia_r(base, exp):
    if exp == 0:
        return 1
    elif exp == 1:
        return base
    else:
        return base * potencia_r(base, exp - 1)

def main():
    try:
        base = float(input("Ingrese el valor de la base: "))
        exp = int(input("Ingrese el valor del exponente: "))
        resultado = potencia_r(base, exp)
        print(f"{base}^{exp} es igual a {resultado}")
    except ValueError:
        print("Por favor, ingrese valores numéricos válidos.")

if __name__ == "__main__":
    main()

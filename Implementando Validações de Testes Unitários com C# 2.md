using System;
using System.Collections.Generic;
using TestesUnitarios.Desafio.Console.Services;
using Xunit;

namespace TestesUnitarios.Desafio.Tests
{
    public class ValidacoesListaTests
    {
        [Fact]
        public void DeveRemoverNumerosNegativosDeUmaLista()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { 1, -2, 3, -4, 5 };

            // Act
            var resultado = validacoesLista.RemoverNumerosNegativos(lista);

            // Assert
            Assert.All(resultado, num => Assert.True(num > 0));
        }

        [Fact]
        public void DeveConterONumero9NaLista()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { 1, 3, 5, 9, 11 };

            // Act
            var resultado = validacoesLista.ListaContemDeterminadoNumero(lista, 9);

            // Assert
            Assert.True(resultado);
        }

        [Fact]
        public void NaoDeveConterONumero10NaLista()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { 1, 3, 5, 9, 11 };

            // Act
            var resultado = validacoesLista.ListaContemDeterminadoNumero(lista, 10);

            // Assert
            Assert.False(resultado);
        }

        [Fact]
        public void DeveMultiplicarOsElementosDaListaPor2()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { 1, 3, 5, 7, 9 };
            var multiplicador = 2;

            // Act
            var resultado = validacoesLista.MultiplicarNumerosLista(lista, multiplicador);

            // Assert
            Assert.Equal(new List<int> { 2, 6, 10, 14, 18 }, resultado);
        }

        [Fact]
        public void DeveRetornar9ComoMaiorNumeroDaLista()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { 1, 3, 5, 9, 7 };

            // Act
            var resultado = validacoesLista.RetornarMaiorNumeroLista(lista);

            // Assert
            Assert.Equal(9, resultado);
        }

        [Fact]
        public void DeveRetornarOitoNegativoComoMenorNumeroDaLista()
        {
            // Arrange
            var validacoesLista = new ValidacoesLista();
            var lista = new List<int> { -2, -8, -6, -4, -5 };

            // Act
            var resultado = validacoesLista.RetornarMenorNumeroLista(lista);

            // Assert
            Assert.Equal(-8, resultado);
        }
    }
}

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: 5008F83F-AF3E-47CF-99A3-55129E654128
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/add-azvmsecret
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Add-AzVMSecret.md
ms.openlocfilehash: b2209b3e9d7c7dcf01a05af277dd5106e70fd8b2
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94279514"
---
# Add-AzVMSecret

## SYNOPSIS
Bir sanal makineye parola ekler.

## INDEKI

```
Add-AzVMSecret [-VM] <PSVirtualMachine> [[-SourceVaultId] <String>] [[-CertificateStore] <String>]
 [[-CertificateUrl] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzVMSecret** cmdlet 'i, bir sanal makineye parola ekler.
Bu değer, sanal makineye sertifika eklemenize olanak tanır.
Gizli anahtar bir kasaya depolanmalıdır.
Anahtar Kasası hakkında daha fazla bilgi için [Azure Anahtar Kasası nedir?](https://azure.microsoft.com/en-us/documentation/articles/key-vault-whatis/)konusuna bakın.
Cmdlet 'ler hakkında daha fazla bilgi için, Microsoft Geliştirici ağ kitaplığında veya [set-Azanahtarvaultsecret](/powershell/module/az.keyvault/set-azkeyvaultsecret) cmdlet 'Inde [Azure Anahtar Kasası cmdlet 'lerini](https://msdn.microsoft.com/library/azure/dn868052.aspx) görebilirsiniz.

## ÖRNEKLERDEN

### Örnek 1: sanal makineye parola ekleme
```
PS C:\> $VirtualMachine = New-AzVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $SourceVaultId = "/subscriptions/46f8cea4-2de6-4179-8ab1-365da4211af4/resourceGroups/vault/providers/Microsoft.KeyVault/vaults/keyvault"
PS C:\> $CertificateStore01 = "My"
PS C:\> $CertificateUrl01 = "https://contosovault.vault.azure.net/secrets/514ceb769c984379a7e0230bdd703272"
PS C:\> $VirtualMachine = Add-AzVMSecret -VM $VirtualMachine -SourceVaultId $SourceVaultId -CertificateStore $CertificateStore01 -CertificateUrl $CertificateUrl01
```

İlk komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.
İkinci komut Get-Credential cmdlet 'ini kullanarak bir kimlik bilgisi nesnesi oluşturur ve sonucu $Credential değişkeninde depolar.
Komut sizden bir Kullanıcı adı ve parola ister.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .
Üçüncü komut, $VirtualMachine depolanan sanal makineyi yapılandırmak için **set-AzVMOperatingSystem** cmdlet 'ini kullanır.
Dördüncü komut daha sonra kullanmak üzere $SourceVaultId değişkenine bir kaynak Kasası KIMLIĞI atar.
Komut $SubscriptionId değişkeninde uygun bir değer olduğunu varsayar.
Beşinci komut, $CertificateStore 01 değişkenine daha sonra kullanmak üzere bir değer atar.
Altıncı komut, sertifika deposu için bir URL atar.
Yedinci komutu, $VirtualMachine depolanan sanal makineye bir parola ekler.
SourceVaultId parametresi Anahtar Kasası belirtir.
Komut, sertifika deposu adını ve sertifikanın URL 'sini belirtir.
Diğer sertifikaların gizlilikleri eklemek için **Add-AzVMSecret** 'i art arda çalıştırabilirsiniz.

## PARAMETRELERINE

### -CertificateStore
Windows işletim sistemini çalıştıran sanal makinedeki bir sertifika depolama adını belirtir.
Bu cmdlet, sertifikayı bu parametrenin belirttiği mağazaya ekler.
Bu parametreyi yalnızca Windows işletim sistemini çalıştıran sanal makineler için belirtebilirsiniz.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -CertificateUrl 'Si
Sertifika içeren bir Anahtar Kasası gizliliğini gösteren URL 'YI belirtir.
Bu sertifika, UTF-8 ile kodlanmış olan aşağıdaki JavaScript nesne gösterimi (JSON) nesnesinin Base64 kodlamasıdır: {"Data": " \<Base64-encoded-file\> ", "DataType": " \<file-format\> ", "Password": " \<pfx-file-password\> "} Şu anda yalnızca. pfx dosyalarını kabul eder.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SourceVaultId
Sanal makineye ekleyebileceğiniz sertifikaları içeren Anahtar Kasası kaynak KIMLIĞINI belirtir.
Bu değer, birden çok sertifika ekleme anahtarı olarak da davranır.
Bu, aynı anahtar kasasından birden çok sertifika eklerken *Sourcevaultid* için aynı değeri kullanabileceğiniz anlamına gelir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Id

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.
Sanal makine nesnesi edinmek için [Get-AzVM](./Get-AzVM.md) cmdlet 'ini kullanın.
Sanal makine nesnesi oluşturmak için [New-AzVMConfig](./New-AzVMConfig.md) cmdlet 'ini kullanabilirsiniz.

```yaml
Type: Microsoft.Azure.Commands.Compute.Models.PSVirtualMachine
Parameter Sets: (All)
Aliases: VMProfile

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

### System. String

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzVM](./Get-AzVM.md)

[New-AzVMConfig](./New-AzVMConfig.md)

[Set-AzVMOperatingSystem](./Set-AzVMOperatingSystem.md)

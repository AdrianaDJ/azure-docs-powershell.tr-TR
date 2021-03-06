---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: 50B64FFE-8277-4DAA-805A-271123B35355
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.compute/add-azurermvmadditionalunattendcontent
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Commands.Compute/help/Add-AzureRmVMAdditionalUnattendContent.md
ms.openlocfilehash: 564f0df5ac5382cdd30b1fcc6d90e713b4bdef91
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589580"
---
# Add-AzureRmVMAdditionalUnattendContent

## SYNOPSIS
Katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## INDEKI

```
Add-AzureRmVMAdditionalUnattendContent [-VM] <PSVirtualMachine> [[-Content] <String>]
 [[-SettingName] <SettingNames>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Add-AzureRmVMAdditionalUnattendContent** cmdlet 'ı katılımsız Windows kurulumu yanıt dosyasına bilgi ekler.
Bu cmdlet unattend.xml dosyaya eklediği ek temel 64 kodlanmış. xml biçimli bilgileri belirtin.

## ÖRNEKLERDEN

### Örnek 1: unattend.xml içerik ekleme
```
PS C:\> $AvailabilitySet = Get-AzureRmAvailabilitySet -ResourceGroupName "ResourceGroup11" -Name "AvailabilitySet03"
PS C:\> $VirtualMachine = New-AzureRmVMConfig -VMName "VirtualMachine07" -VMSize "Standard_A1" -AvailabilitySetID $AvailabilitySet.Id 
PS C:\> $Credential = Get-Credential
PS C:\> $VirtualMachine = Set-AzureRmVMOperatingSystem -VM $VirtualMachine  -Windows -ComputerName "Contoso26" -Credential $Credential
PS C:\> $AucContent = "<UserAccounts><AdministratorPassword><Value>" + "Password" + "</Value><PlainText>true</PlainText></AdministratorPassword></UserAccounts>";
PS C:\> $VirtualMachine = Add-AzureRmVMAdditionalUnattendContent -VM $VirtualMachine -Content $AucContent -SettingName "AutoLogon"
```

İlk komut, ResourceGroup11 adındaki kaynak grubundaki AvailablitySet03 adındaki kullanılabilirlik kümesini alır ve bu nesneyi $AvailabilitySet değişkeninde depolar.
İkinci komut bir sanal makine nesnesi oluşturur ve $VirtualMachine değişkeninde depolar.
Bu komut sanal makineye bir ad ve boyut atar.
Sanal makine, $AvailabilitySet depolanan kullanılabilirlik kümesine aittir.
Üçüncü komut Get-Credential cmdlet 'ini kullanarak bir kimlik bilgisi nesnesi oluşturur ve sonucu $Credential değişkeninde depolar.
Komut sizden bir Kullanıcı adı ve parola ister.
Daha fazla bilgi için yazın `Get-Help Get-Credential` .
Dördüncü komut, $VirtualMachine depolanan sanal makineyi yapılandırmak için **set-AzureRmVMOperatingSystem** cmdlet 'ini kullanır.
Beşinci komut, $AucContent değişkenine içerik atar.
İçerik bir parola içerir.
Son komut $AucContent depolanan içeriği unattend.xml dosyasına ekler.

## PARAMETRELERINE

### -İçerik
Base 64 kodlanmış XML formatlı içeriğini belirtir.
Bu cmdlet içeriği unattend.xml dosyasına ekler.
XML içeriği 4 KB 'den az olmalıdır ve bu cmdlet 'in eklediği ayarın veya özelliğin kök öğesini içermelidir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### -SettingName
İçeriğin uygulandığı ayarın adını belirtir.
Bu parametre için kabul edilebilir değerler şunlardır:
- FirstLogonCommands
- Açmayı

```yaml
Type: System.Nullable`1[Microsoft.Azure.Management.Compute.Models.SettingNames]
Parameter Sets: (All)
Aliases:
Accepted values: AutoLogon, FirstLogonCommands

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -VM
Bu cmdlet 'in değiştirdiği sanal makine nesnesini belirtir.
Sanal makine nesnesi edinmek için [Get-AzureRmVM](./Get-AzureRmVM.md) cmdlet 'ini kullanın.
[New-AzureRmVMConfig](./New-AzureRmVMConfig.md) cmdlet 'ini kullanarak sanal makine nesnesi oluşturun.

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
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

### System. String

### System. Nullable ' 1 [[Microsoft. Azure. Management. COMPUTE. modeller. SettingNames, Microsoft. Azure. Management. COMPUTE, Version = 21.0.0.0, Culture = neutral, PublicKeyToken = 31bf3856ad364e35]]

## ÇıKıŞLAR

### Microsoft. Azure. Commands. COMPUTE. modeller. PSVirtualMachine

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzureRmAvailabilitySet](./Get-AzureRmAvailabilitySet.md)

[Set-AzureRmVMOperatingSystem](./Set-AzureRmVMOperatingSystem.md)

[Yeni-AzureRmVMConfig](./New-AzureRmVMConfig.md)

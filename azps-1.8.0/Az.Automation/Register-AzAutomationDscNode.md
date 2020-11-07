---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Automation.dll-Help.xml
Module Name: Az.Automation
ms.assetid: 73E6DF02-7171-481B-966F-DECEC122A602
online version: https://docs.microsoft.com/en-us/powershell/module/az.automation/register-azautomationdscnode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Automation/Automation/help/Register-AzAutomationDscNode.md
ms.openlocfilehash: 5dc2682597be6f05a65bafc38424139e9707578f
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761548"
---
# Register-AzAutomationDscNode

## SYNOPSIS
Bir Otomasyon hesabı için bir Azure sanal makinesini DSC düğümü olarak kaydeder.

## INDEKI

```
Register-AzAutomationDscNode -AzureVMName <String> [-NodeConfigurationName <String>]
 [-ConfigurationMode <String>] [-ConfigurationModeFrequencyMins <Int32>] [-RefreshFrequencyMins <Int32>]
 [-RebootNodeIfNeeded <Boolean>] [-ActionAfterReboot <String>] [-AllowModuleOverwrite <Boolean>]
 [-AzureVMResourceGroup <String>] [-AzureVMLocation <String>] [-ResourceGroupName] <String>
 [-AutomationAccountName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## Tanım
**Register-AzAutomationDscNode** cmdlet 'i, bir Azure Otomasyonu hesabında bir Azure sanal MAKINESINI bir APS Istenen durum YAPıLANDıRMASı (DSC) düğümü olarak kaydeder.

## ÖRNEKLERDEN

### Örnek 1: Azure sanal makinesini Azure DSC düğümü olarak kaydettirme
```
PS C:\>Register-AzAutomationDscNode -AutomationAccountName "Contoso17" -AzVMName "VirtualMachine01" -ResourceGroupName "ResourceGroup01"-NodeConfigurationName "ContosoConfiguration.webserver"
```

Bu komut VirtualMachine01 adındaki bir Azure sanal makinesini Contoso17 adındaki Otomasyon hesabında DSC düğümü olarak kaydeder.

## PARAMETRELERINE

### -ActionAfterReboot
Yeniden başlatıldıktan sonra sanal makinenin aldığı eylemi belirtir.
Geçerli değerler: 
- Devam yapılandırması 
- Durdurma yapılandırması

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ContinueConfiguration, StopConfiguration

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AllowModuleOverwrite
Bu DSC düğümünün Azure Otomasyonu DSC çekme sunucusundan İndirilme yeni yapılandırmaların, var olan modüllerin hedef düğümde var olan modülleri değiştirip değiştirmeyeceğini belirtir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AutomationAccountName
Bu cmdlet 'in sanal makine kaydettiğinde bir Otomasyon hesabının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMLocation
Azure VM konumu.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMName
Azure Otomasyonu DSC ile yönetim için kaydettiriedilecek Azure sanal makinesinin adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -AzureVMResourceGroup
Azure VM kaynak grubu adı.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ConfigurationMode
DSC yapılandırma modunu belirtir.
Geçerli değerler: 
- Applyandmonitörü 
- ApplyAndAutocorrect 
- Yalnızca Apply

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: ApplyAndMonitor, ApplyAndAutocorrect, ApplyOnly

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Configurationmodeftalep
DSC 'nin arka plan uygulamasının hedef düğümdeki geçerli yapılandırmayı uygulama girişimlerinin dakika cinsinden süresini belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -DefaultProfile
Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik

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

### -NodeConfigurationName
Bu cmdlet 'in sanal makineyi Azure Automation DSC 'den çekme için yapılandırdığını düğümün yapılandırmasının adını belirtir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -Rebootnodeıfgerekli
Gerekirse sanal makinenin yeniden etkinleştirilip etkinleştirilmeyeceğini belirtir.

```yaml
Type: System.Boolean
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -RefreshFrequencyMins
Yerel Configuration Manager 'ın en son düğüm yapılandırmasını indirmek için Azure Otomasyonu DSC istek sunucusuyla iletişim kurduğunda frekansı dakika cinsinden belirtir.

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### -ResourceGroupName
Kaynak grubunun adını belirtir.
Bu cmdlet 'in bir sanal makineyi kaydeden Otomasyon hesabı, bu parametrenin belirttiği kaynak grubuna aittir.

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### CommonParameters
Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken. Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .

## GÖLGELENDIRICI

### System. String

### System. Int32

### System. Boolean

## ÇıKıŞLAR

### System. void

## NOTLARıNDA

## ILGILI BAĞLANTıLAR

[Get-AzAutomationDscNode](./Get-AzAutomationDscNode.md)

[Set-AzAutomationDscNode](./Set-AzAutomationDscNode.md)

[Unregister-AzAutomationDscNode](./Unregister-AzAutomationDscNode.md)



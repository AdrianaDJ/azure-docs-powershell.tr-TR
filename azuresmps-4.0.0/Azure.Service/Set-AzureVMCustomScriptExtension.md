---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 6A8F07D1-AC20-4950-9019-BDFB4FD3CF69
online version: ''
schema: 2.0.0
ms.openlocfilehash: a7569e203369bf1177b4eecc2bd689f3e20dcd48
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106037"
---
# <span data-ttu-id="32a18-101">Set-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="32a18-101">Set-AzureVMCustomScriptExtension</span></span>

## <span data-ttu-id="32a18-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="32a18-102">SYNOPSIS</span></span>
<span data-ttu-id="32a18-103">Azure sanal makinesi özel komut dosyası uzantısı için bilgileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="32a18-103">Sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="32a18-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="32a18-104">SYNTAX</span></span>

### <span data-ttu-id="32a18-105">Setcustomscrip/2 Sionbycontainervedosyaadı (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="32a18-105">SetCustomScriptExtensionByContainerAndFileNames (Default)</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-ContainerName] <String>
 [-FileName] <String[]> [[-StorageAccountName] <String>] [[-StorageEndpointSuffix] <String>]
 [[-StorageAccountKey] <String>] [[-Run] <String>] [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="32a18-106">DisableCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="32a18-106">DisableCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Disable] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="32a18-107">Unınstallecustomscriptextension</span><span class="sxs-lookup"><span data-stu-id="32a18-107">UninstalleCustomScriptExtension</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [-Uninstall] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="32a18-108">Setcustomscripist Sionbyurilmürekkepler</span><span class="sxs-lookup"><span data-stu-id="32a18-108">SetCustomScriptExtensionByUriLinks</span></span>
```
Set-AzureVMCustomScriptExtension [[-ReferenceName] <String>] [[-Version] <String>] [[-FileUri] <String[]>]
 [-Run] <String> [[-Argument] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="32a18-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="32a18-109">DESCRIPTION</span></span>
<span data-ttu-id="32a18-110">**Set-AzureVMCustomScriptExtension** cmdlet 'ı bir Azure sanal makine özel komut dosyası uzantısının bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="32a18-110">The **Set-AzureVMCustomScriptExtension** cmdlet sets information for an Azure virtual machine custom script extension.</span></span>

## <span data-ttu-id="32a18-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="32a18-111">EXAMPLES</span></span>

### <span data-ttu-id="32a18-112">Örnek 1: sanal makine özel Betik uzantısı için bilgileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="32a18-112">Example 1: Set information for a virtual machine custom script extension</span></span>
```
PS C:\> $VM = Set-AzureVMCustomScriptExtension -VM $VM -ContainerName "Container01" -FileName "script1.ps1","script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> New-AzureVM -Location "West US" -ServiceName $SVC -VM $VM;
```

<span data-ttu-id="32a18-113">Bu komut, sanal makine özel komut dosyası uzantısı için bilgileri ayarlar.</span><span class="sxs-lookup"><span data-stu-id="32a18-113">This command sets information for a virtual machine custom script extension.</span></span>

### <span data-ttu-id="32a18-114">Örnek 2: dosya yolu kullanarak sanal makine özel komut dosyası uzantısı için bilgileri ayarlama</span><span class="sxs-lookup"><span data-stu-id="32a18-114">Example 2: Set information for a virtual machine custom script extension using a file path</span></span>
```
PS C:\> Set-AzureVMCustomScriptExtension -VM $VM -FileUri "http://www.blob.core.contoso.net/bar/script1.ps1","http://www.blob.core.contoso.net/baz/script2.ps1" -Run "script1.ps1" -Argument "arg1 arg2";
PS C:\> Update-AzureVM -ServiceName $SVC -Name $Name -VM VM;
```

<span data-ttu-id="32a18-115">Bu komut, birden çok dosya URL 'Si kullanan bir sanal makine özel komut dosyası uzantısının bilgilerini ayarlar.</span><span class="sxs-lookup"><span data-stu-id="32a18-115">This command sets information for a virtual machine custom script extension using multiple file URLs.</span></span>

## <span data-ttu-id="32a18-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="32a18-116">PARAMETERS</span></span>

### <span data-ttu-id="32a18-117">-Bağımsız değişken</span><span class="sxs-lookup"><span data-stu-id="32a18-117">-Argument</span></span>
<span data-ttu-id="32a18-118">Bu cmdlet 'in sanal makinede çalıştığı bağımsız değişkeni sağlayan bir dize belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-118">Specifies a string that supplies an argument that this cmdlet runs on the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames, SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-119">-Kapsayıcıadı</span><span class="sxs-lookup"><span data-stu-id="32a18-119">-ContainerName</span></span>
<span data-ttu-id="32a18-120">Depolama hesabı içinde kapsayıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-120">Specifies the container name within the storage account.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-121">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="32a18-121">-Disable</span></span>
<span data-ttu-id="32a18-122">Bu cmdlet 'in uzantı durumunu devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32a18-122">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-123">-Dosya adı</span><span class="sxs-lookup"><span data-stu-id="32a18-123">-FileName</span></span>
<span data-ttu-id="32a18-124">Belirtilen kapsayıcıdaki blob dosyalarının adlarını içeren bir dize dizisi belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-124">Specifies a string array that contains the names of the blob files in the specified container.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-125">-FileUri</span><span class="sxs-lookup"><span data-stu-id="32a18-125">-FileUri</span></span>
<span data-ttu-id="32a18-126">Blob dosyalarının URL 'Lerini içeren bir dize dizisini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-126">Specifies a string array that contains the URLs of the blob files.</span></span>

```yaml
Type: String[]
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-127">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="32a18-127">-ForceUpdate</span></span>
<span data-ttu-id="32a18-128">Yapılandırma güncelleştirilmemişse, bu cmdlet 'in bir uzantıya yeniden uygulanacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32a18-128">Indicates that this cmdlet re-apply a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-129">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="32a18-129">-InformationAction</span></span>
<span data-ttu-id="32a18-130">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-130">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="32a18-131">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="32a18-131">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="32a18-132">'A</span><span class="sxs-lookup"><span data-stu-id="32a18-132">Continue</span></span>
- <span data-ttu-id="32a18-133">Manıza</span><span class="sxs-lookup"><span data-stu-id="32a18-133">Ignore</span></span>
- <span data-ttu-id="32a18-134">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="32a18-134">Inquire</span></span>
- <span data-ttu-id="32a18-135">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="32a18-135">SilentlyContinue</span></span>
- <span data-ttu-id="32a18-136">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="32a18-136">Stop</span></span>
- <span data-ttu-id="32a18-137">Biliriz</span><span class="sxs-lookup"><span data-stu-id="32a18-137">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-138">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="32a18-138">-InformationVariable</span></span>
<span data-ttu-id="32a18-139">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-139">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-140">-Profil</span><span class="sxs-lookup"><span data-stu-id="32a18-140">-Profile</span></span>
<span data-ttu-id="32a18-141">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-141">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="32a18-142">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="32a18-142">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-143">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="32a18-143">-ReferenceName</span></span>
<span data-ttu-id="32a18-144">Uzantının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-144">Specifies the reference name for the extension.</span></span>

<span data-ttu-id="32a18-145">Bu parametre, uzantıya başvurmak için kullanılabilecek Kullanıcı tanımlı bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="32a18-145">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="32a18-146">Uzantı sanal makineye ilk kez eklendiğinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="32a18-146">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="32a18-147">Sonraki güncelleştirmelerde, uzantıyı güncelleştirirken önceden kullanılmış başvuru adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="32a18-147">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="32a18-148">Uzantıya atanan *ReferenceName* , **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="32a18-148">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-149">-Run</span><span class="sxs-lookup"><span data-stu-id="32a18-149">-Run</span></span>
<span data-ttu-id="32a18-150">Bu cmdlet 'in sanal makinedeki uzantı tarafından çalıştığı komutu belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-150">Specifies the command this cmdlet runs by the extension on the virtual machine.</span></span>
<span data-ttu-id="32a18-151">Yalnızca "powershell.exe" destekleniyor.</span><span class="sxs-lookup"><span data-stu-id="32a18-151">Only "powershell.exe" is supported.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: RunFile, Command

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByUriLinks
Aliases: RunFile, Command

Required: True
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-152">-StorageAccountKey</span><span class="sxs-lookup"><span data-stu-id="32a18-152">-StorageAccountKey</span></span>
<span data-ttu-id="32a18-153">Depolama hesabı anahtarını belirtir</span><span class="sxs-lookup"><span data-stu-id="32a18-153">Specifies the storage account key</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-154">-StorageAccountName</span><span class="sxs-lookup"><span data-stu-id="32a18-154">-StorageAccountName</span></span>
<span data-ttu-id="32a18-155">Geçerli abonelikteki depolama hesabı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-155">Specifies the storage account name in the current subscription.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-156">-StorageEndpointSuffix</span><span class="sxs-lookup"><span data-stu-id="32a18-156">-StorageEndpointSuffix</span></span>
<span data-ttu-id="32a18-157">Depolama hizmeti uç noktasını belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-157">Specifies the storage service endpoint.</span></span>

```yaml
Type: String
Parameter Sets: SetCustomScriptExtensionByContainerAndFileNames
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-158">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="32a18-158">-Uninstall</span></span>
<span data-ttu-id="32a18-159">Bu cmdlet 'in sanal makineden özel betik uzantısını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="32a18-159">Indicates that this cmdlet uninstalls the custom script extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstalleCustomScriptExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-160">-Version</span><span class="sxs-lookup"><span data-stu-id="32a18-160">-Version</span></span>
<span data-ttu-id="32a18-161">Özel komut dosyası uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-161">Specifies the version of the custom script extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-162">-VM</span><span class="sxs-lookup"><span data-stu-id="32a18-162">-VM</span></span>
<span data-ttu-id="32a18-163">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="32a18-163">Specifies the persistent virtual machine object.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="32a18-164">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="32a18-164">CommonParameters</span></span>
<span data-ttu-id="32a18-165">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="32a18-165">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="32a18-166">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="32a18-166">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="32a18-167">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="32a18-167">INPUTS</span></span>

## <span data-ttu-id="32a18-168">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="32a18-168">OUTPUTS</span></span>

## <span data-ttu-id="32a18-169">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="32a18-169">NOTES</span></span>

## <span data-ttu-id="32a18-170">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="32a18-170">RELATED LINKS</span></span>

[<span data-ttu-id="32a18-171">Get-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="32a18-171">Get-AzureVMCustomScriptExtension</span></span>](./Get-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="32a18-172">Remove-AzureVMCustomScriptExtension</span><span class="sxs-lookup"><span data-stu-id="32a18-172">Remove-AzureVMCustomScriptExtension</span></span>](./Remove-AzureVMCustomScriptExtension.md)

[<span data-ttu-id="32a18-173">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="32a18-173">Get-AzureVM</span></span>](./Get-AzureVM.md)



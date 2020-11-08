---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 97E9FB22-43A8-4D07-AF48-5884E4593CA9
online version: ''
schema: 2.0.0
ms.openlocfilehash: 35f3baea7440d58812056999ea4f271acf80b8d4
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105446"
---
# <span data-ttu-id="37434-101">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="37434-101">Set-AzureVMExtension</span></span>

## <span data-ttu-id="37434-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="37434-102">SYNOPSIS</span></span>
<span data-ttu-id="37434-103">Sanal makinelerin kaynak uzantılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="37434-103">Sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="37434-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="37434-104">SYNTAX</span></span>

### <span data-ttu-id="37434-105">SetByExtensionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="37434-105">SetByExtensionName (Default)</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfiguration] <String>] [[-PrivateConfiguration] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="37434-106">SetByExtensionNameAndConfigFile</span><span class="sxs-lookup"><span data-stu-id="37434-106">SetByExtensionNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [-Version] <String>
 [[-ReferenceName] <String>] [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>] [-Disable]
 [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="37434-107">SetByReferenceName</span><span class="sxs-lookup"><span data-stu-id="37434-107">SetByReferenceName</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfiguration] <String>]
 [[-PrivateConfiguration] <String>] [-Disable] [-Uninstall] [[-PublicConfigKey] <String>]
 [[-PrivateConfigKey] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="37434-108">Setbyreferencenadeniz Vseçconfigfile</span><span class="sxs-lookup"><span data-stu-id="37434-108">SetByReferenceNameAndConfigFile</span></span>
```
Set-AzureVMExtension [-ReferenceName] <String> [[-PublicConfigPath] <String>] [[-PrivateConfigPath] <String>]
 [-Disable] [-Uninstall] [[-PublicConfigKey] <String>] [[-PrivateConfigKey] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="37434-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="37434-109">DESCRIPTION</span></span>
<span data-ttu-id="37434-110">**Set-AzureVMExtension** cmdlet 'i sanal makinelerin kaynak uzantılarını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="37434-110">The **Set-AzureVMExtension** cmdlet sets resource extensions for virtual machines.</span></span>

## <span data-ttu-id="37434-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="37434-111">EXAMPLES</span></span>

### <span data-ttu-id="37434-112">Örnek 1: kaynak uzantıları uygulanmış sanal makine oluşturma</span><span class="sxs-lookup"><span data-stu-id="37434-112">Example 1: Create a virtual machine with resource extensions applied</span></span>
```
PS C:\> $X = New-AzureVMConfig -Name $VM -InstanceSize Small -ImageName $IMG;$X = Add-AzureProvisioningConfig -VM $X -Password $PWD -AdminUsername $USR -Windows;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext1 -Publisher $Publisher -Version $VER -PublicConfiguration $P1 -PrivateConfiguration $P2;$X = Set-AzureVMExtension -VM $X -ExtensionName $Ext2 -Publisher $Publisher -Version $VER -PublicConfiguration $P3 -PrivateConfiguration $P4;New-AzureVM -Location $LOC -ServiceName $SVC -VM $X;
```

<span data-ttu-id="37434-113">Bu komut, kaynak uzantıları uygulanmış bir sanal makine oluşturur.</span><span class="sxs-lookup"><span data-stu-id="37434-113">This command creates a virtual machine with resource extensions applied.</span></span>

## <span data-ttu-id="37434-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="37434-114">PARAMETERS</span></span>

### <span data-ttu-id="37434-115">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="37434-115">-Disable</span></span>
<span data-ttu-id="37434-116">Bu cmdlet 'in uzantı durumunu devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37434-116">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 7
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-117">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="37434-117">-ExtensionName</span></span>
<span data-ttu-id="37434-118">Sanal makinenin uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-118">Specifies the extension name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-119">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="37434-119">-ForceUpdate</span></span>
<span data-ttu-id="37434-120">Yapılandırma güncelleştirilmediyse, bu cmdlet 'in bir uzantıya yeniden uyguladığı anlamına gelir.</span><span class="sxs-lookup"><span data-stu-id="37434-120">Indicates that this cmdlet re-applies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 11
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="37434-121">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="37434-121">-InformationAction</span></span>
<span data-ttu-id="37434-122">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-122">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="37434-123">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="37434-123">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="37434-124">'A</span><span class="sxs-lookup"><span data-stu-id="37434-124">Continue</span></span>
- <span data-ttu-id="37434-125">Manıza</span><span class="sxs-lookup"><span data-stu-id="37434-125">Ignore</span></span>
- <span data-ttu-id="37434-126">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="37434-126">Inquire</span></span>
- <span data-ttu-id="37434-127">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="37434-127">SilentlyContinue</span></span>
- <span data-ttu-id="37434-128">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="37434-128">Stop</span></span>
- <span data-ttu-id="37434-129">Biliriz</span><span class="sxs-lookup"><span data-stu-id="37434-129">Suspend</span></span>

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

### <span data-ttu-id="37434-130">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="37434-130">-InformationVariable</span></span>
<span data-ttu-id="37434-131">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-131">Specifies an information variable.</span></span>

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

### <span data-ttu-id="37434-132">-PrivateConfigKey</span><span class="sxs-lookup"><span data-stu-id="37434-132">-PrivateConfigKey</span></span>
<span data-ttu-id="37434-133">Özel bir konfigürasyon anahtarı belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-133">Specifies a private configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 10
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-134">-PrivateConfigPath</span><span class="sxs-lookup"><span data-stu-id="37434-134">-PrivateConfigPath</span></span>
<span data-ttu-id="37434-135">Özel yapılandırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-135">Specifies the private configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-136">-PrivateConfiguration</span><span class="sxs-lookup"><span data-stu-id="37434-136">-PrivateConfiguration</span></span>
<span data-ttu-id="37434-137">Özel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-137">Specifies the private configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 6
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-138">-Profil</span><span class="sxs-lookup"><span data-stu-id="37434-138">-Profile</span></span>
<span data-ttu-id="37434-139">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-139">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="37434-140">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="37434-140">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="37434-141">-PublicConfigKey</span><span class="sxs-lookup"><span data-stu-id="37434-141">-PublicConfigKey</span></span>
<span data-ttu-id="37434-142">Genel yapılandırma anahtarını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-142">Specifies the public configuration key.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 9
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-143">-PublicConfigPath</span><span class="sxs-lookup"><span data-stu-id="37434-143">-PublicConfigPath</span></span>
<span data-ttu-id="37434-144">Genel yapılandırma yolunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-144">Specifies the public configuration path.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionNameAndConfigFile, SetByReferenceNameAndConfigFile
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-145">-PublicConfiguration</span><span class="sxs-lookup"><span data-stu-id="37434-145">-PublicConfiguration</span></span>
<span data-ttu-id="37434-146">Genel yapılandırma metnini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-146">Specifies the public configuration text.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByReferenceName
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-147">-Publisher</span><span class="sxs-lookup"><span data-stu-id="37434-147">-Publisher</span></span>
<span data-ttu-id="37434-148">Uzantının yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-148">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-149">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="37434-149">-ReferenceName</span></span>
<span data-ttu-id="37434-150">Uzantının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-150">Specifies the reference name of the extension.</span></span>

<span data-ttu-id="37434-151">Bu, uzantıya başvurmak için kullanılabilecek Kullanıcı tanımlı bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="37434-151">This is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="37434-152">Uzantı sanal makineye ilk kez eklendiğinde belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="37434-152">You need to specify it when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="37434-153">Sonraki güncelleştirmelerde, uzantıyı güncelleştirirken önceden kullanılmış başvuru adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="37434-153">For subsequent updates, you need to specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="37434-154">Uzantıya atanan ReferenceName, **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="37434-154">The ReferenceName assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: SetByReferenceName, SetByReferenceNameAndConfigFile
Aliases: 

Required: True
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-155">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="37434-155">-Uninstall</span></span>
<span data-ttu-id="37434-156">Bu cmdlet 'in sanal makineden kaynak uzantısını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="37434-156">Indicates that this cmdlet uninstalls the resource extension from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 8
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-157">-Version</span><span class="sxs-lookup"><span data-stu-id="37434-157">-Version</span></span>
<span data-ttu-id="37434-158">Uzantı sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-158">Specifies the extension version.</span></span>

```yaml
Type: String
Parameter Sets: SetByExtensionName, SetByExtensionNameAndConfigFile
Aliases: 

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="37434-159">-VM</span><span class="sxs-lookup"><span data-stu-id="37434-159">-VM</span></span>
<span data-ttu-id="37434-160">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="37434-160">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="37434-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="37434-161">CommonParameters</span></span>
<span data-ttu-id="37434-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="37434-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="37434-163">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="37434-163">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="37434-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="37434-164">INPUTS</span></span>

## <span data-ttu-id="37434-165">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="37434-165">OUTPUTS</span></span>

## <span data-ttu-id="37434-166">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="37434-166">NOTES</span></span>

## <span data-ttu-id="37434-167">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="37434-167">RELATED LINKS</span></span>

[<span data-ttu-id="37434-168">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="37434-168">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="37434-169">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="37434-169">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="37434-170">Get-AzureVM</span><span class="sxs-lookup"><span data-stu-id="37434-170">Get-AzureVM</span></span>](./Get-AzureVM.md)



---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8F881112-3603-4EE7-88A4-ED45040A60AC
online version: ''
schema: 2.0.0
ms.openlocfilehash: ecc71708c0dff8e359813bb01db0f09f2c91a0cb
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105811"
---
# <span data-ttu-id="b6021-101">Set-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b6021-101">Set-AzureVMAccessExtension</span></span>

## <span data-ttu-id="b6021-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b6021-102">SYNOPSIS</span></span>
<span data-ttu-id="b6021-103">Sanal makinenin VMAccess uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6021-103">Sets the VMAccess extension for a virtual machine.</span></span>

## <span data-ttu-id="b6021-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b6021-104">SYNTAX</span></span>

### <span data-ttu-id="b6021-105">Enableaccessextenma (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="b6021-105">EnableAccessExtension (Default)</span></span>
```
Set-AzureVMAccessExtension [[-UserName] <String>] [[-Password] <String>] [[-ReferenceName] <String>]
 [[-Version] <String>] [-ForceUpdate] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6021-106">Disableaccessexten</span><span class="sxs-lookup"><span data-stu-id="b6021-106">DisableAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="b6021-107">Unınstallaccessextenma</span><span class="sxs-lookup"><span data-stu-id="b6021-107">UninstallAccessExtension</span></span>
```
Set-AzureVMAccessExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] [-ForceUpdate]
 -VM <IPersistentVM> [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>]
 [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="b6021-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="b6021-108">DESCRIPTION</span></span>
<span data-ttu-id="b6021-109">**Set-AzureVMAccessExtension** cmdlet 'i sanal makine VMAccess uzantısını bir sanal makineye ekler.</span><span class="sxs-lookup"><span data-stu-id="b6021-109">The **Set-AzureVMAccessExtension** cmdlet adds the Virtual Machine VMAccess Extension to a virtual machine.</span></span> <span data-ttu-id="b6021-110">VMAccess uzantısı geçici bir parola ayarlamak için kullanılabilir ve bu, makinede oturum açıldıktan sonra hemen değiştirilmelidir.</span><span class="sxs-lookup"><span data-stu-id="b6021-110">VMAccess Extension can be used to set a temporary password and this should be immediately changed it after logging into the machine.</span></span>

## <span data-ttu-id="b6021-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b6021-111">EXAMPLES</span></span>

### <span data-ttu-id="b6021-112">Örnek 1: belirli bir sanal makineye uygulanan VMAccess uzantısı 'nı ayarlama</span><span class="sxs-lookup"><span data-stu-id="b6021-112">Example 1: Set the VMAccess extension applied to a specified virtual machine</span></span>
```
PS C:\> Set-AzureVMAccessExtension -VM $VM -UserName $User -Password $PWD;
```

<span data-ttu-id="b6021-113">Bu komut, belirtilen sanal makineye, $VM değişkeninde depolanan VMAccess uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="b6021-113">This command sets the VMAccess extension applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="b6021-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b6021-114">PARAMETERS</span></span>

### <span data-ttu-id="b6021-115">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="b6021-115">-Disable</span></span>
<span data-ttu-id="b6021-116">Bu cmdlet 'in uzantı durumunu devre dışı olarak ayarladiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-116">Indicates that this cmdlet sets the Extension State to Disable.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: DisableAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-117">-ForceUpdate</span><span class="sxs-lookup"><span data-stu-id="b6021-117">-ForceUpdate</span></span>
<span data-ttu-id="b6021-118">Yapılandırma güncelleştirilmemişse, bu cmdlet 'in bir yapılandırmayı uzantıya yeniden etkinleştirdiğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-118">Indicates that this cmdlet reapplies a configuration to an extension when the configuration has not been updated.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: 5
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-119">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="b6021-119">-InformationAction</span></span>
<span data-ttu-id="b6021-120">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-120">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="b6021-121">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="b6021-121">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="b6021-122">'A</span><span class="sxs-lookup"><span data-stu-id="b6021-122">Continue</span></span>
- <span data-ttu-id="b6021-123">Manıza</span><span class="sxs-lookup"><span data-stu-id="b6021-123">Ignore</span></span>
- <span data-ttu-id="b6021-124">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="b6021-124">Inquire</span></span>
- <span data-ttu-id="b6021-125">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="b6021-125">SilentlyContinue</span></span>
- <span data-ttu-id="b6021-126">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="b6021-126">Stop</span></span>
- <span data-ttu-id="b6021-127">Biliriz</span><span class="sxs-lookup"><span data-stu-id="b6021-127">Suspend</span></span>

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

### <span data-ttu-id="b6021-128">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="b6021-128">-InformationVariable</span></span>
<span data-ttu-id="b6021-129">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-129">Specifies an information variable.</span></span>

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

### <span data-ttu-id="b6021-130">-Parola</span><span class="sxs-lookup"><span data-stu-id="b6021-130">-Password</span></span>
<span data-ttu-id="b6021-131">Sanal makinenin kimlik bilgisini sıfırlamak için parolayı belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-131">Specifies the password for resetting the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-132">-Profil</span><span class="sxs-lookup"><span data-stu-id="b6021-132">-Profile</span></span>
<span data-ttu-id="b6021-133">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-133">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="b6021-134">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="b6021-134">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="b6021-135">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="b6021-135">-ReferenceName</span></span>
<span data-ttu-id="b6021-136">Access uzantısının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-136">Specifies the reference name of the access extension.</span></span>

<span data-ttu-id="b6021-137">Bu, uzantıya başvurmak için kullanılan Kullanıcı tanımlı bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="b6021-137">This is a user-defined string that is used to refer to an extension.</span></span>
<span data-ttu-id="b6021-138">Uzantı sanal makineye ilk kez eklendiğinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="b6021-138">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="b6021-139">Sonraki güncelleştirmelerde, uzantıyı güncelleştirirken önceden kullanılmış başvuru adını belirtmeniz gerekir.</span><span class="sxs-lookup"><span data-stu-id="b6021-139">For subsequent updates, you should specify the previously used reference name while updating the extension.</span></span>
<span data-ttu-id="b6021-140">Uzantıya atanan *ReferenceName* , **Get-AzureVM** cmdlet 'i kullanılarak döndürülür.</span><span class="sxs-lookup"><span data-stu-id="b6021-140">The *ReferenceName* assigned to an extension is returned using the **Get-AzureVM** cmdlet.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-141">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="b6021-141">-Uninstall</span></span>
<span data-ttu-id="b6021-142">Bu cmdlet 'in Access uzantısını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b6021-142">Indicates whether this cmdlet uninstalls the access extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallAccessExtension
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-143">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="b6021-143">-UserName</span></span>
<span data-ttu-id="b6021-144">Sanal makinenin kimlik bilgilerini sıfırlamak için bu cmdlet 'in kullandığı kullanıcı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-144">Specifies the user name that this cmdlet uses to reset the virtual machine's credential.</span></span>

```yaml
Type: String
Parameter Sets: EnableAccessExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-145">-Version</span><span class="sxs-lookup"><span data-stu-id="b6021-145">-Version</span></span>
<span data-ttu-id="b6021-146">Uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-146">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b6021-147">-VM</span><span class="sxs-lookup"><span data-stu-id="b6021-147">-VM</span></span>
<span data-ttu-id="b6021-148">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="b6021-148">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="b6021-149">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b6021-149">CommonParameters</span></span>
<span data-ttu-id="b6021-150">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b6021-150">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b6021-151">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b6021-151">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b6021-152">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b6021-152">INPUTS</span></span>

## <span data-ttu-id="b6021-153">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b6021-153">OUTPUTS</span></span>

## <span data-ttu-id="b6021-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b6021-154">NOTES</span></span>

## <span data-ttu-id="b6021-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b6021-155">RELATED LINKS</span></span>

[<span data-ttu-id="b6021-156">Get-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b6021-156">Get-AzureVMAccessExtension</span></span>](./Get-AzureVMAccessExtension.md)

[<span data-ttu-id="b6021-157">Remove-AzureVMAccessExtension</span><span class="sxs-lookup"><span data-stu-id="b6021-157">Remove-AzureVMAccessExtension</span></span>](./Remove-AzureVMAccessExtension.md)



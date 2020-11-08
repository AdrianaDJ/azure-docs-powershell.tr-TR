---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 377716B6-8B8C-4CAE-A8FA-835DA24F04C7
online version: ''
schema: 2.0.0
ms.openlocfilehash: c9610c6b8abaf4d59d6a363253d0b90a0dfcecad
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106043"
---
# <span data-ttu-id="388cc-101">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="388cc-101">Set-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="388cc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="388cc-102">SYNOPSIS</span></span>
<span data-ttu-id="388cc-103">Sanal makinenin BgInfo uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="388cc-103">Sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="388cc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="388cc-104">SYNTAX</span></span>

### <span data-ttu-id="388cc-105">SetBGInfoExtension (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="388cc-105">SetBGInfoExtension (Default)</span></span>
```
Set-AzureVMBGInfoExtension [-Disable] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="388cc-106">UninstallBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="388cc-106">UninstallBGInfoExtension</span></span>
```
Set-AzureVMBGInfoExtension [-Uninstall] [[-ReferenceName] <String>] [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="388cc-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="388cc-107">DESCRIPTION</span></span>
<span data-ttu-id="388cc-108">**Set-AzureVMBGInfoExtension** cmdlet 'i sanal makinenin BgInfo uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="388cc-108">The **Set-AzureVMBGInfoExtension** cmdlet sets the BGInfo extension for a virtual machine.</span></span>

## <span data-ttu-id="388cc-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="388cc-109">EXAMPLES</span></span>

### <span data-ttu-id="388cc-110">Örnek 1: sanal makine için BgInfo uzantısını ayarlama</span><span class="sxs-lookup"><span data-stu-id="388cc-110">Example 1: Set the BGInfo extension for a virtual machine</span></span>
```
PS C:\> Set-AzureVMBGInfoExtension -VM $VM
```

<span data-ttu-id="388cc-111">Bu komut, belirtilen sanal makinenin $VM değişkende depolanan BgInfo uzantısını ayarlar.</span><span class="sxs-lookup"><span data-stu-id="388cc-111">This command sets the BGInfo extension for the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="388cc-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="388cc-112">PARAMETERS</span></span>

### <span data-ttu-id="388cc-113">-Devre dışı bırak</span><span class="sxs-lookup"><span data-stu-id="388cc-113">-Disable</span></span>
<span data-ttu-id="388cc-114">Bu cmdlet 'in uzantı durumunu devre dışı bırakacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="388cc-114">Indicates that this cmdlet disables the extension state.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: SetBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388cc-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="388cc-115">-InformationAction</span></span>
<span data-ttu-id="388cc-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="388cc-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="388cc-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="388cc-118">'A</span><span class="sxs-lookup"><span data-stu-id="388cc-118">Continue</span></span>
- <span data-ttu-id="388cc-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="388cc-119">Ignore</span></span>
- <span data-ttu-id="388cc-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="388cc-120">Inquire</span></span>
- <span data-ttu-id="388cc-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="388cc-121">SilentlyContinue</span></span>
- <span data-ttu-id="388cc-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="388cc-122">Stop</span></span>
- <span data-ttu-id="388cc-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="388cc-123">Suspend</span></span>

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

### <span data-ttu-id="388cc-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="388cc-124">-InformationVariable</span></span>
<span data-ttu-id="388cc-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="388cc-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="388cc-126">-Profile</span></span>
<span data-ttu-id="388cc-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="388cc-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="388cc-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="388cc-129">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="388cc-129">-ReferenceName</span></span>
<span data-ttu-id="388cc-130">BgInfo uzantısının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-130">Specifies the reference name of the BGInfo extension.</span></span>

<span data-ttu-id="388cc-131">Bu parametre, uzantıya başvurmak için kullanılabilecek Kullanıcı tanımlı bir dizedir.</span><span class="sxs-lookup"><span data-stu-id="388cc-131">This parameter is a user-defined string that can be used to refer to an extension.</span></span>
<span data-ttu-id="388cc-132">Uzantı sanal makineye ilk kez eklendiğinde belirtilir.</span><span class="sxs-lookup"><span data-stu-id="388cc-132">It is specified when the extension is added to the virtual machine for the first time.</span></span>
<span data-ttu-id="388cc-133">Uzantıyı güncelleştirirken daha önce kullanılmış olan başvuru adını belirtebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="388cc-133">You can specify the previously used reference name while updating the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388cc-134">-Uninstall</span><span class="sxs-lookup"><span data-stu-id="388cc-134">-Uninstall</span></span>
<span data-ttu-id="388cc-135">Bu cmdlet 'in BgInfo uzantısını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="388cc-135">Indicates that this cmdlet uninstalls the BGInfo extension.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: UninstallBGInfoExtension
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="388cc-136">-Version</span><span class="sxs-lookup"><span data-stu-id="388cc-136">-Version</span></span>
<span data-ttu-id="388cc-137">BgInfo uzantısının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-137">Specifies the version of the BGInfo extension.</span></span>

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

### <span data-ttu-id="388cc-138">-VM</span><span class="sxs-lookup"><span data-stu-id="388cc-138">-VM</span></span>
<span data-ttu-id="388cc-139">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="388cc-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="388cc-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="388cc-140">CommonParameters</span></span>
<span data-ttu-id="388cc-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="388cc-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="388cc-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="388cc-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="388cc-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="388cc-143">INPUTS</span></span>

## <span data-ttu-id="388cc-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="388cc-144">OUTPUTS</span></span>

## <span data-ttu-id="388cc-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="388cc-145">NOTES</span></span>

## <span data-ttu-id="388cc-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="388cc-146">RELATED LINKS</span></span>

[<span data-ttu-id="388cc-147">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="388cc-147">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="388cc-148">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="388cc-148">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)



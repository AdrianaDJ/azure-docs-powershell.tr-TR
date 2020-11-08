---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: B98FCF46-A5D6-4CC9-B82A-60B429A21A8B
online version: ''
schema: 2.0.0
ms.openlocfilehash: 8079844a931debee5b9338e98d405697cc4336f2
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105501"
---
# <span data-ttu-id="5e79c-101">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="5e79c-101">Remove-AzureVMExtension</span></span>

## <span data-ttu-id="5e79c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5e79c-102">SYNOPSIS</span></span>
<span data-ttu-id="5e79c-103">Sanal makineden kaynak uzantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e79c-103">Removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="5e79c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5e79c-104">SYNTAX</span></span>

### <span data-ttu-id="5e79c-105">RemoveByExtensionName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="5e79c-105">RemoveByExtensionName (Default)</span></span>
```
Remove-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

### <span data-ttu-id="5e79c-106">RemoveByReferenceName</span><span class="sxs-lookup"><span data-stu-id="5e79c-106">RemoveByReferenceName</span></span>
```
Remove-AzureVMExtension [-ReferenceName] <String> -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="5e79c-107">RemoveAll</span><span class="sxs-lookup"><span data-stu-id="5e79c-107">RemoveAll</span></span>
```
Remove-AzureVMExtension [-RemoveAll] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5e79c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="5e79c-108">DESCRIPTION</span></span>
<span data-ttu-id="5e79c-109">**Remove-AzureVMExtension** cmdlet 'i sanal bir makineden kaynak uzantılarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e79c-109">The **Remove-AzureVMExtension** cmdlet removes resource extensions from a virtual machine.</span></span>

## <span data-ttu-id="5e79c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5e79c-110">EXAMPLES</span></span>

### <span data-ttu-id="5e79c-111">Örnek 1: belirli bir ad ve yayıncı kullanarak uzantıyı kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e79c-111">Example 1: Remove an extension using a specific name and publisher</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -ExtensionName $EXT -Publisher $PUB;
```

<span data-ttu-id="5e79c-112">Bu komut, belirtilen ad ve yayımcıya sahip bir uzantıyı kaldırır.</span><span class="sxs-lookup"><span data-stu-id="5e79c-112">This command removes an extension with the specified name and publisher.</span></span>

### <span data-ttu-id="5e79c-113">Örnek 2: belirli bir sanal makinedeki tüm uzantıları kaldırma</span><span class="sxs-lookup"><span data-stu-id="5e79c-113">Example 2: Remove all extensions from a specific virtual machine</span></span>
```
PS C:\> $VM = Remove-AzureVMExtension -VM $VM -RemoveAll;
```

<span data-ttu-id="5e79c-114">Bu komut, belirtilen sanal makinedeki tüm uzantıları, $VM değişkeninde depolanır.</span><span class="sxs-lookup"><span data-stu-id="5e79c-114">This command removes all extensions from the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="5e79c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5e79c-115">PARAMETERS</span></span>

### <span data-ttu-id="5e79c-116">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="5e79c-116">-ExtensionName</span></span>
<span data-ttu-id="5e79c-117">Bu cmdlet 'in kaldırıldığı uzantı adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-117">Specifies the extension name that this cmdlet removes.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e79c-118">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5e79c-118">-InformationAction</span></span>
<span data-ttu-id="5e79c-119">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-119">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5e79c-120">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5e79c-120">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5e79c-121">'A</span><span class="sxs-lookup"><span data-stu-id="5e79c-121">Continue</span></span>
- <span data-ttu-id="5e79c-122">Manıza</span><span class="sxs-lookup"><span data-stu-id="5e79c-122">Ignore</span></span>
- <span data-ttu-id="5e79c-123">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="5e79c-123">Inquire</span></span>
- <span data-ttu-id="5e79c-124">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="5e79c-124">SilentlyContinue</span></span>
- <span data-ttu-id="5e79c-125">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="5e79c-125">Stop</span></span>
- <span data-ttu-id="5e79c-126">Biliriz</span><span class="sxs-lookup"><span data-stu-id="5e79c-126">Suspend</span></span>

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

### <span data-ttu-id="5e79c-127">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="5e79c-127">-InformationVariable</span></span>
<span data-ttu-id="5e79c-128">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-128">Specifies an information variable.</span></span>

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

### <span data-ttu-id="5e79c-129">-Profil</span><span class="sxs-lookup"><span data-stu-id="5e79c-129">-Profile</span></span>
<span data-ttu-id="5e79c-130">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-130">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5e79c-131">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5e79c-131">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="5e79c-132">-Publisher</span><span class="sxs-lookup"><span data-stu-id="5e79c-132">-Publisher</span></span>
<span data-ttu-id="5e79c-133">Uzantı yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-133">Specifies the extension publisher.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e79c-134">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="5e79c-134">-ReferenceName</span></span>
<span data-ttu-id="5e79c-135">Uzantının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-135">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: RemoveByReferenceName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e79c-136">-RemoveAll</span><span class="sxs-lookup"><span data-stu-id="5e79c-136">-RemoveAll</span></span>
<span data-ttu-id="5e79c-137">Bu cmdlet 'in sanal makinedeki tüm kaynak uzantılarını kaldırmadığını gösterir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-137">Indicates that this cmdlet removes all resource extensions from the virtual machine.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: RemoveAll
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5e79c-138">-VM</span><span class="sxs-lookup"><span data-stu-id="5e79c-138">-VM</span></span>
<span data-ttu-id="5e79c-139">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5e79c-139">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="5e79c-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5e79c-140">CommonParameters</span></span>
<span data-ttu-id="5e79c-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5e79c-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5e79c-142">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5e79c-142">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5e79c-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5e79c-143">INPUTS</span></span>

## <span data-ttu-id="5e79c-144">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5e79c-144">OUTPUTS</span></span>

## <span data-ttu-id="5e79c-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5e79c-145">NOTES</span></span>

## <span data-ttu-id="5e79c-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5e79c-146">RELATED LINKS</span></span>

[<span data-ttu-id="5e79c-147">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="5e79c-147">Get-AzureVMExtension</span></span>](./Get-AzureVMExtension.md)

[<span data-ttu-id="5e79c-148">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="5e79c-148">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)



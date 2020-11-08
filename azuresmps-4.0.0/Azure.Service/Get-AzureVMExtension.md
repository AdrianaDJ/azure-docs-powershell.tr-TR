---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 7ED074F0-1E9E-40C2-A543-D19A49831DD3
online version: ''
schema: 2.0.0
ms.openlocfilehash: 2f0b8ca9acfe5a62b002944bd44e11acfcd38ec1
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94106533"
---
# <span data-ttu-id="a331d-101">Get-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="a331d-101">Get-AzureVMExtension</span></span>

## <span data-ttu-id="a331d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a331d-102">SYNOPSIS</span></span>
<span data-ttu-id="a331d-103">Sanal makinelere uygulanan kaynak uzantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a331d-103">Gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="a331d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a331d-104">SYNTAX</span></span>

### <span data-ttu-id="a331d-105">ListByReferenceName (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="a331d-105">ListByReferenceName (Default)</span></span>
```
Get-AzureVMExtension [[-ReferenceName] <String>] -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

### <span data-ttu-id="a331d-106">ListByExtensionName</span><span class="sxs-lookup"><span data-stu-id="a331d-106">ListByExtensionName</span></span>
```
Get-AzureVMExtension [-ExtensionName] <String> [-Publisher] <String> [[-Version] <String>] -VM <IPersistentVM>
 [-Profile <AzureSMProfile>] [-InformationAction <ActionPreference>] [-InformationVariable <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="a331d-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="a331d-107">DESCRIPTION</span></span>
<span data-ttu-id="a331d-108">**Get-AzureVMExtension** cmdlet 'i sanal makinelere uygulanan kaynak uzantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a331d-108">The **Get-AzureVMExtension** cmdlet gets resource extensions applied to virtual machines.</span></span>

## <span data-ttu-id="a331d-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a331d-109">EXAMPLES</span></span>

### <span data-ttu-id="a331d-110">Örnek 1: sanal makineye uygulanan kaynak uzantılarını alma</span><span class="sxs-lookup"><span data-stu-id="a331d-110">Example 1: Get the resource extensions applied to a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName $SVC -Name $VM | Get-AzureVMExtension;
```

<span data-ttu-id="a331d-111">Bu komut, $VM değişkeninde depolanan belirtilen sanal makineye uygulanan kaynak uzantılarını alır.</span><span class="sxs-lookup"><span data-stu-id="a331d-111">This command gets the resource extensions applied to the specified virtual machine as stored in the variable $VM.</span></span>

## <span data-ttu-id="a331d-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a331d-112">PARAMETERS</span></span>

### <span data-ttu-id="a331d-113">-ExtensionName</span><span class="sxs-lookup"><span data-stu-id="a331d-113">-ExtensionName</span></span>
<span data-ttu-id="a331d-114">Sanal makine uzantısının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-114">Specifies the virtual machine extension name.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a331d-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a331d-115">-InformationAction</span></span>
<span data-ttu-id="a331d-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a331d-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a331d-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a331d-118">'A</span><span class="sxs-lookup"><span data-stu-id="a331d-118">Continue</span></span>
- <span data-ttu-id="a331d-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="a331d-119">Ignore</span></span>
- <span data-ttu-id="a331d-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a331d-120">Inquire</span></span>
- <span data-ttu-id="a331d-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a331d-121">SilentlyContinue</span></span>
- <span data-ttu-id="a331d-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a331d-122">Stop</span></span>
- <span data-ttu-id="a331d-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a331d-123">Suspend</span></span>

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

### <span data-ttu-id="a331d-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a331d-124">-InformationVariable</span></span>
<span data-ttu-id="a331d-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-125">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a331d-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="a331d-126">-Profile</span></span>
<span data-ttu-id="a331d-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a331d-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a331d-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a331d-129">-Publisher</span><span class="sxs-lookup"><span data-stu-id="a331d-129">-Publisher</span></span>
<span data-ttu-id="a331d-130">Uzantının yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-130">Specifies the publisher of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a331d-131">-ReferenceName</span><span class="sxs-lookup"><span data-stu-id="a331d-131">-ReferenceName</span></span>
<span data-ttu-id="a331d-132">Uzantının başvuru adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-132">Specifies the reference name of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByReferenceName
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a331d-133">-Version</span><span class="sxs-lookup"><span data-stu-id="a331d-133">-Version</span></span>
<span data-ttu-id="a331d-134">Uzantının sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-134">Specifies the version of the extension.</span></span>

```yaml
Type: String
Parameter Sets: ListByExtensionName
Aliases: 

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a331d-135">-VM</span><span class="sxs-lookup"><span data-stu-id="a331d-135">-VM</span></span>
<span data-ttu-id="a331d-136">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a331d-136">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a331d-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a331d-137">CommonParameters</span></span>
<span data-ttu-id="a331d-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a331d-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a331d-139">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a331d-139">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a331d-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a331d-140">INPUTS</span></span>

## <span data-ttu-id="a331d-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a331d-141">OUTPUTS</span></span>

## <span data-ttu-id="a331d-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a331d-142">NOTES</span></span>

## <span data-ttu-id="a331d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a331d-143">RELATED LINKS</span></span>

[<span data-ttu-id="a331d-144">Remove-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="a331d-144">Remove-AzureVMExtension</span></span>](./Remove-AzureVMExtension.md)

[<span data-ttu-id="a331d-145">Set-AzureVMExtension</span><span class="sxs-lookup"><span data-stu-id="a331d-145">Set-AzureVMExtension</span></span>](./Set-AzureVMExtension.md)



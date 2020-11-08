---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8C735528-3844-452F-983B-41AC5CD4E414
online version: ''
schema: 2.0.0
ms.openlocfilehash: 1ea39b2c06a5daf7540009f480e7c2ec211e7f47
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105508"
---
# <span data-ttu-id="862cd-101">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="862cd-101">Remove-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="862cd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="862cd-102">SYNOPSIS</span></span>
<span data-ttu-id="862cd-103">Sanal makineye uygulanan BgInfo uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="862cd-103">Removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="862cd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="862cd-104">SYNTAX</span></span>

```
Remove-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="862cd-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="862cd-105">DESCRIPTION</span></span>
<span data-ttu-id="862cd-106">**Remove-AzureVMBGInfoExtension** cmdlet 'i, bir sanal makineye uygulanan BgInfo uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="862cd-106">The **Remove-AzureVMBGInfoExtension** cmdlet removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="862cd-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="862cd-107">EXAMPLES</span></span>

### <span data-ttu-id="862cd-108">Örnek 1: sanal makinedeki BgInfo uzantısını kaldırma</span><span class="sxs-lookup"><span data-stu-id="862cd-108">Example 1: Remove the BGInfo extension on a virtual machine</span></span>
```
PS C:\> Remove-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="862cd-109">Bu komut, bir sanal makineye uygulanan BgInfo uzantısını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="862cd-109">This command removes the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="862cd-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="862cd-110">PARAMETERS</span></span>

### <span data-ttu-id="862cd-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="862cd-111">-InformationAction</span></span>
<span data-ttu-id="862cd-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="862cd-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="862cd-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="862cd-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="862cd-114">'A</span><span class="sxs-lookup"><span data-stu-id="862cd-114">Continue</span></span>
- <span data-ttu-id="862cd-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="862cd-115">Ignore</span></span>
- <span data-ttu-id="862cd-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="862cd-116">Inquire</span></span>
- <span data-ttu-id="862cd-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="862cd-117">SilentlyContinue</span></span>
- <span data-ttu-id="862cd-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="862cd-118">Stop</span></span>
- <span data-ttu-id="862cd-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="862cd-119">Suspend</span></span>

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

### <span data-ttu-id="862cd-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="862cd-120">-InformationVariable</span></span>
<span data-ttu-id="862cd-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="862cd-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="862cd-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="862cd-122">-Profile</span></span>
<span data-ttu-id="862cd-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="862cd-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="862cd-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="862cd-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="862cd-125">-VM</span><span class="sxs-lookup"><span data-stu-id="862cd-125">-VM</span></span>
<span data-ttu-id="862cd-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="862cd-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="862cd-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="862cd-127">CommonParameters</span></span>
<span data-ttu-id="862cd-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="862cd-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="862cd-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="862cd-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="862cd-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="862cd-130">INPUTS</span></span>

## <span data-ttu-id="862cd-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="862cd-131">OUTPUTS</span></span>

## <span data-ttu-id="862cd-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="862cd-132">NOTES</span></span>

## <span data-ttu-id="862cd-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="862cd-133">RELATED LINKS</span></span>

[<span data-ttu-id="862cd-134">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="862cd-134">Get-AzureVMBGInfoExtension</span></span>](./Get-AzureVMBGInfoExtension.md)

[<span data-ttu-id="862cd-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="862cd-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)



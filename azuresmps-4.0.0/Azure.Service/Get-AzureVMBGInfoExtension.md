---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: E4CB958B-AC85-4036-A6D6-002FAF40BB66
online version: ''
schema: 2.0.0
ms.openlocfilehash: 5e74be3310b895ef4c941a59541a64f9c6d1b279
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105532"
---
# <span data-ttu-id="a10e4-101">Get-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a10e4-101">Get-AzureVMBGInfoExtension</span></span>

## <span data-ttu-id="a10e4-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a10e4-102">SYNOPSIS</span></span>
<span data-ttu-id="a10e4-103">Bir sanal makineye uygulanan BgInfo uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="a10e4-103">Gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a10e4-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a10e4-104">SYNTAX</span></span>

```
Get-AzureVMBGInfoExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="a10e4-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a10e4-105">DESCRIPTION</span></span>
<span data-ttu-id="a10e4-106">**Get-AzureVMBGInfoExtension** cmdlet 'i, bir sanal makineye uygulanan BgInfo uzantısını alır.</span><span class="sxs-lookup"><span data-stu-id="a10e4-106">The **Get-AzureVMBGInfoExtension** cmdlet gets the BGInfo extension applied on a virtual machine.</span></span>

## <span data-ttu-id="a10e4-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a10e4-107">EXAMPLES</span></span>

### <span data-ttu-id="a10e4-108">Örnek 1: belirli bir sanal makineye uygulanan BgInfo uzantısını alma</span><span class="sxs-lookup"><span data-stu-id="a10e4-108">Example 1: Get the BGInfo extension applied on a specified virtual machine</span></span>
```
PS C:\> Get-AzureVMBGInfoExtension -VM $VM;
```

<span data-ttu-id="a10e4-109">Bu komut, belirtilen sanal makineye uygulanan BgInfo uzantısını alır</span><span class="sxs-lookup"><span data-stu-id="a10e4-109">This command gets the BGInfo extension applied on a specified virtual machine</span></span>

## <span data-ttu-id="a10e4-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a10e4-110">PARAMETERS</span></span>

### <span data-ttu-id="a10e4-111">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="a10e4-111">-InformationAction</span></span>
<span data-ttu-id="a10e4-112">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a10e4-112">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="a10e4-113">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="a10e4-113">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="a10e4-114">'A</span><span class="sxs-lookup"><span data-stu-id="a10e4-114">Continue</span></span>
- <span data-ttu-id="a10e4-115">Manıza</span><span class="sxs-lookup"><span data-stu-id="a10e4-115">Ignore</span></span>
- <span data-ttu-id="a10e4-116">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="a10e4-116">Inquire</span></span>
- <span data-ttu-id="a10e4-117">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="a10e4-117">SilentlyContinue</span></span>
- <span data-ttu-id="a10e4-118">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="a10e4-118">Stop</span></span>
- <span data-ttu-id="a10e4-119">Biliriz</span><span class="sxs-lookup"><span data-stu-id="a10e4-119">Suspend</span></span>

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

### <span data-ttu-id="a10e4-120">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="a10e4-120">-InformationVariable</span></span>
<span data-ttu-id="a10e4-121">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="a10e4-121">Specifies an information variable.</span></span>

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

### <span data-ttu-id="a10e4-122">-Profil</span><span class="sxs-lookup"><span data-stu-id="a10e4-122">-Profile</span></span>
<span data-ttu-id="a10e4-123">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a10e4-123">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="a10e4-124">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="a10e4-124">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

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

### <span data-ttu-id="a10e4-125">-VM</span><span class="sxs-lookup"><span data-stu-id="a10e4-125">-VM</span></span>
<span data-ttu-id="a10e4-126">Kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="a10e4-126">Specifies the persistent virtual machine object.</span></span>

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

### <span data-ttu-id="a10e4-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a10e4-127">CommonParameters</span></span>
<span data-ttu-id="a10e4-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a10e4-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a10e4-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a10e4-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a10e4-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a10e4-130">INPUTS</span></span>

## <span data-ttu-id="a10e4-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a10e4-131">OUTPUTS</span></span>

## <span data-ttu-id="a10e4-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a10e4-132">NOTES</span></span>

## <span data-ttu-id="a10e4-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a10e4-133">RELATED LINKS</span></span>

[<span data-ttu-id="a10e4-134">Remove-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a10e4-134">Remove-AzureVMBGInfoExtension</span></span>](./Remove-AzureVMBGInfoExtension.md)

[<span data-ttu-id="a10e4-135">Set-AzureVMBGInfoExtension</span><span class="sxs-lookup"><span data-stu-id="a10e4-135">Set-AzureVMBGInfoExtension</span></span>](./Set-AzureVMBGInfoExtension.md)



---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: 678e08df94d7ea828b04d55892cb66e1c0a62349
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571757"
---
# <span data-ttu-id="e5938-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e5938-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="e5938-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e5938-102">SYNOPSIS</span></span>
<span data-ttu-id="e5938-103">AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="e5938-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="e5938-104">Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.</span><span class="sxs-lookup"><span data-stu-id="e5938-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="e5938-105">Açıkça kabul edilmedikçe veri toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="e5938-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="e5938-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e5938-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e5938-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="e5938-107">DESCRIPTION</span></span>
<span data-ttu-id="e5938-108">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="e5938-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="e5938-109">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzureRmDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi uyarır.</span><span class="sxs-lookup"><span data-stu-id="e5938-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="e5938-110">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="e5938-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="e5938-111">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="e5938-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="e5938-112">Geçerli makinedeki geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzureRMDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e5938-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="e5938-113">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="e5938-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="e5938-114">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzureRmDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="e5938-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="e5938-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e5938-115">EXAMPLES</span></span>

### <span data-ttu-id="e5938-116">Örnek 1: geçerli kullanıcı için veri toplamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="e5938-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="e5938-117">Bu örnekte, geçerli kullanıcı için veri toplamayı etkinleştirme gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="e5938-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="e5938-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e5938-118">PARAMETERS</span></span>

### <span data-ttu-id="e5938-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="e5938-119">-Confirm</span></span>
<span data-ttu-id="e5938-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e5938-120">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5938-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e5938-121">-WhatIf</span></span>
<span data-ttu-id="e5938-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e5938-122">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="e5938-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e5938-123">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="e5938-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e5938-124">CommonParameters</span></span>
<span data-ttu-id="e5938-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e5938-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e5938-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e5938-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e5938-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e5938-127">INPUTS</span></span>

## <span data-ttu-id="e5938-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e5938-128">OUTPUTS</span></span>

### <span data-ttu-id="e5938-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="e5938-129">None</span></span>

## <span data-ttu-id="e5938-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e5938-130">NOTES</span></span>

## <span data-ttu-id="e5938-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e5938-131">RELATED LINKS</span></span>

[<span data-ttu-id="e5938-132">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="e5938-132">Disable-AzureRmDataCollection</span></span>]()


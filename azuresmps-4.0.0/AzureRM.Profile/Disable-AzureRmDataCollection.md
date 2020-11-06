---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
online version: ''
schema: 2.0.0
ms.openlocfilehash: e233c523e5fd9372b1e7dd86b5b5e73eb3f7091e
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93571761"
---
# <span data-ttu-id="9c401-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="9c401-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="9c401-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c401-102">SYNOPSIS</span></span>
<span data-ttu-id="9c401-103">AzurePowerShell cmdlet 'lerini geliştirmek için veri toplama dışında.</span><span class="sxs-lookup"><span data-stu-id="9c401-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="9c401-104">Açıkça kabul etmediğiniz sürece veriler toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="9c401-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="9c401-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c401-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="9c401-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c401-106">DESCRIPTION</span></span>
<span data-ttu-id="9c401-107">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c401-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="9c401-108">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzureRmDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi uyarır.</span><span class="sxs-lookup"><span data-stu-id="9c401-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="9c401-109">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="9c401-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="9c401-110">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="9c401-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>

<span data-ttu-id="9c401-111">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzureRMDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9c401-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="9c401-112">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="9c401-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>

<span data-ttu-id="9c401-113">Geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzureRmDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="9c401-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="9c401-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c401-114">EXAMPLES</span></span>

### <span data-ttu-id="9c401-115">Örnek 1: geçerli kullanıcı için veri toplamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="9c401-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="9c401-116">Bu örnekte, geçerli kullanıcı için veri toplamayı devre dışı bırakma gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="9c401-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="9c401-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c401-117">PARAMETERS</span></span>

### <span data-ttu-id="9c401-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="9c401-118">-Confirm</span></span>
<span data-ttu-id="9c401-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="9c401-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="9c401-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="9c401-120">-WhatIf</span></span>
<span data-ttu-id="9c401-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="9c401-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="9c401-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="9c401-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="9c401-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c401-123">CommonParameters</span></span>
<span data-ttu-id="9c401-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c401-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c401-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c401-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c401-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c401-126">INPUTS</span></span>

## <span data-ttu-id="9c401-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c401-127">OUTPUTS</span></span>

### <span data-ttu-id="9c401-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9c401-128">None</span></span>

## <span data-ttu-id="9c401-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c401-129">NOTES</span></span>

## <span data-ttu-id="9c401-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c401-130">RELATED LINKS</span></span>

[<span data-ttu-id="9c401-131">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="9c401-131">Enable-AzureRmDataCollection</span></span>]()


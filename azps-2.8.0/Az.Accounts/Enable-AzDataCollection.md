---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/enable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Enable-AzDataCollection.md
ms.openlocfilehash: 1a68b5ca391e6c09673f07f0469035e0f96c1562
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753743"
---
# <span data-ttu-id="f1627-101">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f1627-101">Enable-AzDataCollection</span></span>

## <span data-ttu-id="f1627-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f1627-102">SYNOPSIS</span></span>
<span data-ttu-id="f1627-103">AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="f1627-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="f1627-104">Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.</span><span class="sxs-lookup"><span data-stu-id="f1627-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="f1627-105">Açıkça kabul edilmedikçe veri toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="f1627-105">No data is collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="f1627-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f1627-106">SYNTAX</span></span>

```
Enable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f1627-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="f1627-107">DESCRIPTION</span></span>
<span data-ttu-id="f1627-108">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f1627-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="f1627-109">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi sorduğunda, açıkça kabul etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="f1627-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="f1627-110">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="f1627-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="f1627-111">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="f1627-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="f1627-112">Geçerli makinedeki geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f1627-112">Run the Enable-AzDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="f1627-113">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="f1627-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="f1627-114">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="f1627-114">To disable data collection for the current user, run the Disable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="f1627-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f1627-115">EXAMPLES</span></span>

### <span data-ttu-id="f1627-116">Örnek 1: geçerli kullanıcı için veri toplamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="f1627-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzDataCollection
```

<span data-ttu-id="f1627-117">Bu örnekte, geçerli kullanıcı için veri toplamayı etkinleştirme gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="f1627-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="f1627-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f1627-118">PARAMETERS</span></span>

### <span data-ttu-id="f1627-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f1627-119">-DefaultProfile</span></span>
<span data-ttu-id="f1627-120">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f1627-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.Core.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1627-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="f1627-121">-Confirm</span></span>
<span data-ttu-id="f1627-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f1627-122">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1627-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f1627-123">-WhatIf</span></span>
<span data-ttu-id="f1627-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f1627-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="f1627-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f1627-125">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f1627-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f1627-126">CommonParameters</span></span>
<span data-ttu-id="f1627-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f1627-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f1627-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f1627-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f1627-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f1627-129">INPUTS</span></span>

### <span data-ttu-id="f1627-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f1627-130">None</span></span>

## <span data-ttu-id="f1627-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f1627-131">OUTPUTS</span></span>

### <span data-ttu-id="f1627-132">System. void</span><span class="sxs-lookup"><span data-stu-id="f1627-132">System.Void</span></span>

## <span data-ttu-id="f1627-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f1627-133">NOTES</span></span>

## <span data-ttu-id="f1627-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f1627-134">RELATED LINKS</span></span>

[<span data-ttu-id="f1627-135">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="f1627-135">Disable-AzDataCollection</span></span>](./Disable-AzDataCollection.md)


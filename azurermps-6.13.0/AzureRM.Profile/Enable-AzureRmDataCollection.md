---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/enable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Enable-AzureRmDataCollection.md
ms.openlocfilehash: 83c7bda6c7b41f857bac9b63afcca07baa6ecd93
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594345"
---
# <span data-ttu-id="67ff8-101">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="67ff8-101">Enable-AzureRmDataCollection</span></span>

## <span data-ttu-id="67ff8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="67ff8-102">SYNOPSIS</span></span>
<span data-ttu-id="67ff8-103">AzurePowerShell cmdlet 'leriyle Kullanıcı deneyimini geliştirmek için Azure PowerShell 'in veri toplamasını olanaklı kılar.</span><span class="sxs-lookup"><span data-stu-id="67ff8-103">Enables Azure PowerShell to collect data to improve the user experience with AzurePowerShell cmdlets.</span></span>
<span data-ttu-id="67ff8-104">Geçerli bilgisayarda geçerli kullanıcının veri koleksiyonunda bu cmdlet 'i yürütme.</span><span class="sxs-lookup"><span data-stu-id="67ff8-104">Executing this cmdlet opts in to data collection for the current user on the current machine.</span></span>
<span data-ttu-id="67ff8-105">Açıkça kabul edilmedikçe veri toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="67ff8-105">No data is collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="67ff8-106">INDEKI</span><span class="sxs-lookup"><span data-stu-id="67ff8-106">SYNTAX</span></span>

```
Enable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="67ff8-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="67ff8-107">DESCRIPTION</span></span>
<span data-ttu-id="67ff8-108">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="67ff8-108">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="67ff8-109">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzureRmDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi uyarır.</span><span class="sxs-lookup"><span data-stu-id="67ff8-109">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="67ff8-110">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="67ff8-110">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="67ff8-111">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="67ff8-111">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="67ff8-112">Geçerli makinedeki geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzureRMDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="67ff8-112">Run the Enable-AzureRMDataCollection cmdlet to enable data collection for the current user on the current machine.</span></span>
<span data-ttu-id="67ff8-113">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="67ff8-113">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="67ff8-114">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzureRmDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="67ff8-114">To disable data collection for the current user, run the Disable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="67ff8-115">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="67ff8-115">EXAMPLES</span></span>

### <span data-ttu-id="67ff8-116">Örnek 1: geçerli kullanıcı için veri toplamayı etkinleştirme</span><span class="sxs-lookup"><span data-stu-id="67ff8-116">Example 1: Enabling data collection for the current user</span></span>
```
PS C:\> Enable-AzureRmDataCollection
```

<span data-ttu-id="67ff8-117">Bu örnekte, geçerli kullanıcı için veri toplamayı etkinleştirme gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="67ff8-117">This example shows how to enable data collection for the current user.</span></span>

## <span data-ttu-id="67ff8-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="67ff8-118">PARAMETERS</span></span>

### <span data-ttu-id="67ff8-119">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="67ff8-119">-DefaultProfile</span></span>
<span data-ttu-id="67ff8-120">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="67ff8-120">The credentials, account, tenant and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="67ff8-121">-Onay</span><span class="sxs-lookup"><span data-stu-id="67ff8-121">-Confirm</span></span>
<span data-ttu-id="67ff8-122">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="67ff8-122">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="67ff8-123">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="67ff8-123">-WhatIf</span></span>
<span data-ttu-id="67ff8-124">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="67ff8-124">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="67ff8-125">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="67ff8-125">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="67ff8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="67ff8-126">CommonParameters</span></span>
<span data-ttu-id="67ff8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="67ff8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="67ff8-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="67ff8-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="67ff8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="67ff8-129">INPUTS</span></span>

### <span data-ttu-id="67ff8-130">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="67ff8-130">None</span></span>

## <span data-ttu-id="67ff8-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="67ff8-131">OUTPUTS</span></span>

### <span data-ttu-id="67ff8-132">System. void</span><span class="sxs-lookup"><span data-stu-id="67ff8-132">System.Void</span></span>

## <span data-ttu-id="67ff8-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="67ff8-133">NOTES</span></span>

## <span data-ttu-id="67ff8-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="67ff8-134">RELATED LINKS</span></span>

[<span data-ttu-id="67ff8-135">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="67ff8-135">Disable-AzureRmDataCollection</span></span>](./Disable-AzureRmDataCollection.md)


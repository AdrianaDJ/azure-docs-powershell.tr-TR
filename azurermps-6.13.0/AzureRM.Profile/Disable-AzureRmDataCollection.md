---
external help file: Microsoft.Azure.Commands.Profile.dll-Help.xml
Module Name: AzureRM.Profile
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.profile/disable-azurermdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Profile/Commands.Profile/help/Disable-AzureRmDataCollection.md
ms.openlocfilehash: 751dc5f8d75a498f843ebd7e543503c871cad1c5
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594347"
---
# <span data-ttu-id="14dbf-101">Disable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="14dbf-101">Disable-AzureRmDataCollection</span></span>

## <span data-ttu-id="14dbf-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="14dbf-102">SYNOPSIS</span></span>
<span data-ttu-id="14dbf-103">AzurePowerShell cmdlet 'lerini geliştirmek için veri toplama dışında.</span><span class="sxs-lookup"><span data-stu-id="14dbf-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="14dbf-104">Açıkça kabul etmediğiniz sürece veriler toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="14dbf-104">Data is not collected unless you explicitly opt in.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="14dbf-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="14dbf-105">SYNTAX</span></span>

```
Disable-AzureRmDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="14dbf-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="14dbf-106">DESCRIPTION</span></span>
<span data-ttu-id="14dbf-107">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="14dbf-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="14dbf-108">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzureRmDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi uyarır.</span><span class="sxs-lookup"><span data-stu-id="14dbf-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzureRmDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="14dbf-109">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="14dbf-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="14dbf-110">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="14dbf-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="14dbf-111">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzureRMDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="14dbf-111">Run the Disable-AzureRMDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="14dbf-112">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="14dbf-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="14dbf-113">Geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzureRmDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="14dbf-113">To enable data collection for the current user, run the Enable-AzureRmDataCollection cmdlet.</span></span>

## <span data-ttu-id="14dbf-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="14dbf-114">EXAMPLES</span></span>

### <span data-ttu-id="14dbf-115">Örnek 1: geçerli kullanıcı için veri toplamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="14dbf-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzureRmDataCollection
```

<span data-ttu-id="14dbf-116">Bu örnekte, geçerli kullanıcı için veri toplamayı devre dışı bırakma gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="14dbf-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="14dbf-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="14dbf-117">PARAMETERS</span></span>

### <span data-ttu-id="14dbf-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="14dbf-118">-DefaultProfile</span></span>
<span data-ttu-id="14dbf-119">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="14dbf-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="14dbf-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="14dbf-120">-Confirm</span></span>
<span data-ttu-id="14dbf-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="14dbf-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="14dbf-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="14dbf-122">-WhatIf</span></span>
<span data-ttu-id="14dbf-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="14dbf-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="14dbf-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="14dbf-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="14dbf-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="14dbf-125">CommonParameters</span></span>
<span data-ttu-id="14dbf-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="14dbf-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="14dbf-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="14dbf-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="14dbf-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="14dbf-128">INPUTS</span></span>

### <span data-ttu-id="14dbf-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="14dbf-129">None</span></span>

## <span data-ttu-id="14dbf-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="14dbf-130">OUTPUTS</span></span>

### <span data-ttu-id="14dbf-131">System. void</span><span class="sxs-lookup"><span data-stu-id="14dbf-131">System.Void</span></span>

## <span data-ttu-id="14dbf-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="14dbf-132">NOTES</span></span>

## <span data-ttu-id="14dbf-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="14dbf-133">RELATED LINKS</span></span>

[<span data-ttu-id="14dbf-134">Enable-AzureRmDataCollection</span><span class="sxs-lookup"><span data-stu-id="14dbf-134">Enable-AzureRmDataCollection</span></span>](./Enable-AzureRmDataCollection.md)


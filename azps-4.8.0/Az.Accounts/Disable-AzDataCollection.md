---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 27b3565191d7de110a5ba3a1e37d204fe3301cbf
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267411"
---
# <span data-ttu-id="b4c92-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="b4c92-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="b4c92-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b4c92-102">SYNOPSIS</span></span>
<span data-ttu-id="b4c92-103">Azure PowerShell cmdlet 'lerini geliştirmek için veri toplama dışında.</span><span class="sxs-lookup"><span data-stu-id="b4c92-103">Opts out of collecting data to improve the Azure PowerShell cmdlets.</span></span> <span data-ttu-id="b4c92-104">Siz açıkça geri belirtmediğiniz sürece veriler varsayılan olarak toplanır.</span><span class="sxs-lookup"><span data-stu-id="b4c92-104">Data is collected by default unless you explicitly opt out.</span></span>

## <span data-ttu-id="b4c92-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b4c92-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="b4c92-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="b4c92-106">DESCRIPTION</span></span>

<span data-ttu-id="b4c92-107">`Disable-AzDataCollection`Cmdlet veri toplamayı geri çevirmek için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="b4c92-107">The `Disable-AzDataCollection` cmdlet is used to opt out of data collection.</span></span> <span data-ttu-id="b4c92-108">Azure PowerShell varsayılan olarak telemetri verilerini otomatik olarak toplar.</span><span class="sxs-lookup"><span data-stu-id="b4c92-108">Azure PowerShell automatically collects telemetry data by default.</span></span> <span data-ttu-id="b4c92-109">Veri toplamayı devre dışı bırakmak için, açıkça geri almalısınız. Microsoft, kullanım düzenlerini belirlemek, yaygın sorunları belirlemek ve Azure PowerShell 'in deneyimini geliştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="b4c92-109">To disable data collection, you must explicitly opt-out. Microsoft aggregates collected data to identify patterns of usage, to identify common issues, and to improve the experience of Azure PowerShell.</span></span> <span data-ttu-id="b4c92-110">Microsoft Azure PowerShell hiçbir özel veya kişisel veri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="b4c92-110">Microsoft Azure PowerShell doesn't collect any private or personal data.</span></span> <span data-ttu-id="b4c92-111">Daha önce kabul ettiyseniz, `Enable-AzDataCollection` geçerli makinedeki geçerli kullanıcının veri toplamayı yeniden etkinleştirmek için cmdlet 'i çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="b4c92-111">If you've previously opted out, run the `Enable-AzDataCollection` cmdlet to re-enable data collection for the current user on the current machine.</span></span>

## <span data-ttu-id="b4c92-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b4c92-112">EXAMPLES</span></span>

### <span data-ttu-id="b4c92-113">Örnek 1: geçerli kullanıcı için veri toplamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="b4c92-113">Example 1: Disabling data collection for the current user</span></span>

<span data-ttu-id="b4c92-114">Aşağıdaki örnekte, geçerli kullanıcı için veri toplamayı devre dışı bırakma gösterilmiştir.</span><span class="sxs-lookup"><span data-stu-id="b4c92-114">The following example shows how to disable data collection for the current user.</span></span>

```powershell
Disable-AzDataCollection
```

## <span data-ttu-id="b4c92-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b4c92-115">PARAMETERS</span></span>

### <span data-ttu-id="b4c92-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b4c92-116">-DefaultProfile</span></span>

<span data-ttu-id="b4c92-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b4c92-117">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="b4c92-118">-Onay</span><span class="sxs-lookup"><span data-stu-id="b4c92-118">-Confirm</span></span>

<span data-ttu-id="b4c92-119">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="b4c92-119">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="b4c92-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="b4c92-120">-WhatIf</span></span>

<span data-ttu-id="b4c92-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="b4c92-121">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="b4c92-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="b4c92-122">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="b4c92-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b4c92-123">CommonParameters</span></span>

<span data-ttu-id="b4c92-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b4c92-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b4c92-125">Daha fazla bilgi için [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters)bakın.</span><span class="sxs-lookup"><span data-stu-id="b4c92-125">For more information, see [about_CommonParameters](/powershell/module/microsoft.powershell.core/about/about_commonparameters).</span></span>

## <span data-ttu-id="b4c92-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b4c92-126">INPUTS</span></span>

### <span data-ttu-id="b4c92-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b4c92-127">None</span></span>

## <span data-ttu-id="b4c92-128">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b4c92-128">OUTPUTS</span></span>

### <span data-ttu-id="b4c92-129">System. void</span><span class="sxs-lookup"><span data-stu-id="b4c92-129">System.Void</span></span>

## <span data-ttu-id="b4c92-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b4c92-130">NOTES</span></span>

## <span data-ttu-id="b4c92-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b4c92-131">RELATED LINKS</span></span>

[<span data-ttu-id="b4c92-132">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="b4c92-132">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)

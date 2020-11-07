---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Accounts.dll-Help.xml
Module Name: Az.Accounts
online version: https://docs.microsoft.com/en-us/powershell/module/az.accounts/disable-azdatacollection
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Accounts/Accounts/help/Disable-AzDataCollection.md
ms.openlocfilehash: 8c168027573c0160519c8600e3e55cac534edeca
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935269"
---
# <span data-ttu-id="47a6d-101">Disable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="47a6d-101">Disable-AzDataCollection</span></span>

## <span data-ttu-id="47a6d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47a6d-102">SYNOPSIS</span></span>
<span data-ttu-id="47a6d-103">AzurePowerShell cmdlet 'lerini geliştirmek için veri toplama dışında.</span><span class="sxs-lookup"><span data-stu-id="47a6d-103">Opts out of collecting data to improve the AzurePowerShell cmdlets.</span></span> <span data-ttu-id="47a6d-104">Açıkça kabul etmediğiniz sürece veriler toplanmaz.</span><span class="sxs-lookup"><span data-stu-id="47a6d-104">Data is not collected unless you explicitly opt in.</span></span>

## <span data-ttu-id="47a6d-105">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47a6d-105">SYNTAX</span></span>

```
Disable-AzDataCollection [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47a6d-106">Tanım</span><span class="sxs-lookup"><span data-stu-id="47a6d-106">DESCRIPTION</span></span>
<span data-ttu-id="47a6d-107">Veri toplamayı kullanarak Microsoft bulut ve Azure PowerShell 'i kullanma deneyimini geliştirebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="47a6d-107">You can improve the experience of using the Microsoft Cloud and Azure PowerShell by opting in to data collection.</span></span>
<span data-ttu-id="47a6d-108">Azure PowerShell, izniniz olmadan verileri toplamaz; Enable-AzDataCollection 'ı yürüterek veya Evet 'i yanıtlayarak, Azure PowerShell ilk kez cmdlet 'i yürüttüğünüzde veri toplama konusunda sizi sorduğunda, açıkça kabul etmelisiniz.</span><span class="sxs-lookup"><span data-stu-id="47a6d-108">Azure PowerShell does not collect data without your consent - you must explicitly opt in by executing Enable-AzDataCollection, or by answering yes when Azure PowerShell prompts you about collecting data the first time you execute a cmdlet.</span></span>
<span data-ttu-id="47a6d-109">Microsoft toplanan verileri, yaygın sorunları belirlemek ve Azure PowerShell kullanma deneyimini iyileştirmek için toplanan verileri toplar.</span><span class="sxs-lookup"><span data-stu-id="47a6d-109">Microsoft aggregates collected data to identify patterns of usage, to identify common issues and to improve the experience of using Azure PowerShell.</span></span>
<span data-ttu-id="47a6d-110">Microsoft Azure PowerShell herhangi bir özel veri veya herhangi bir kişisel bilgileri toplamaz.</span><span class="sxs-lookup"><span data-stu-id="47a6d-110">Microsoft Azure PowerShell does not collect any private data, or any personally identifiable information.</span></span>
<span data-ttu-id="47a6d-111">Geçerli kullanıcının veri toplamayı devre dışı bırakmak için Disable-AzDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="47a6d-111">Run the Disable-AzDataCollection cmdlet to disable data collection for the current user.</span></span>
<span data-ttu-id="47a6d-112">Bu, geçerli kullanıcıdan veri toplama hakkında bilgi gönderilmesini önleyecektir; ilk cmdlet 'ler yürütülür.</span><span class="sxs-lookup"><span data-stu-id="47a6d-112">This will prevent the current user from being prompted about data collection the first time cmdlets are executed.</span></span>
<span data-ttu-id="47a6d-113">Geçerli kullanıcının veri toplamayı etkinleştirmek için Enable-AzDataCollection cmdlet 'ini çalıştırın.</span><span class="sxs-lookup"><span data-stu-id="47a6d-113">To enable data collection for the current user, run the Enable-AzDataCollection cmdlet.</span></span>

## <span data-ttu-id="47a6d-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47a6d-114">EXAMPLES</span></span>

### <span data-ttu-id="47a6d-115">Örnek 1: geçerli kullanıcı için veri toplamayı devre dışı bırakma</span><span class="sxs-lookup"><span data-stu-id="47a6d-115">Example 1: Disabling data collection for the current user</span></span>
```
PS C:\> Disable-AzDataCollection
```

<span data-ttu-id="47a6d-116">Bu örnekte, geçerli kullanıcı için veri toplamayı devre dışı bırakma gösterilmektedir.</span><span class="sxs-lookup"><span data-stu-id="47a6d-116">This example shows how to disable data collection for the current user.</span></span> 

## <span data-ttu-id="47a6d-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47a6d-117">PARAMETERS</span></span>

### <span data-ttu-id="47a6d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47a6d-118">-DefaultProfile</span></span>
<span data-ttu-id="47a6d-119">Azure ile iletişimde kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47a6d-119">The credentials, account, tenant and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="47a6d-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="47a6d-120">-Confirm</span></span>
<span data-ttu-id="47a6d-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47a6d-121">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47a6d-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47a6d-122">-WhatIf</span></span>
<span data-ttu-id="47a6d-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47a6d-123">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="47a6d-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47a6d-124">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47a6d-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47a6d-125">CommonParameters</span></span>
<span data-ttu-id="47a6d-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47a6d-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47a6d-127">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47a6d-127">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47a6d-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47a6d-128">INPUTS</span></span>

### <span data-ttu-id="47a6d-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="47a6d-129">None</span></span>

## <span data-ttu-id="47a6d-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47a6d-130">OUTPUTS</span></span>

### <span data-ttu-id="47a6d-131">System. void</span><span class="sxs-lookup"><span data-stu-id="47a6d-131">System.Void</span></span>

## <span data-ttu-id="47a6d-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47a6d-132">NOTES</span></span>

## <span data-ttu-id="47a6d-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47a6d-133">RELATED LINKS</span></span>

[<span data-ttu-id="47a6d-134">Enable-AzDataCollection</span><span class="sxs-lookup"><span data-stu-id="47a6d-134">Enable-AzDataCollection</span></span>](./Enable-AzDataCollection.md)


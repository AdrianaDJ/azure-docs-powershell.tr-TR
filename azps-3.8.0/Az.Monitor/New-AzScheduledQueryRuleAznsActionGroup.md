---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azscheduledqueryruleaznsactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzScheduledQueryRuleAznsActionGroup.md
ms.openlocfilehash: 44f9eae56c822e5fe068679331bcdd3a0ad17d81
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94095871"
---
# <span data-ttu-id="a782e-101">New-AzScheduledQueryRuleAznsActionGroup</span><span class="sxs-lookup"><span data-stu-id="a782e-101">New-AzScheduledQueryRuleAznsActionGroup</span></span>

## <span data-ttu-id="a782e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a782e-102">SYNOPSIS</span></span>
<span data-ttu-id="a782e-103">Azns eylem grubu türünde bir nesne oluşturur</span><span class="sxs-lookup"><span data-stu-id="a782e-103">Creates an object of type Azns Action Group</span></span>

## <span data-ttu-id="a782e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a782e-104">SYNTAX</span></span>

```
New-AzScheduledQueryRuleAznsActionGroup [-ActionGroup <String[]>] [-EmailSubject <String>]
 [-CustomWebhookPayload <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a782e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a782e-105">DESCRIPTION</span></span>
<span data-ttu-id="a782e-106">Azns eylem grubu türünde bir nesne oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a782e-106">Creates an object of type Azns Action Group.</span></span>
<span data-ttu-id="a782e-107">Bu nesne, günlük uyarı kuralı oluşturan komuta geçirilir.</span><span class="sxs-lookup"><span data-stu-id="a782e-107">This object is to be passed to the command that creates Log Alert Rule.</span></span>

## <span data-ttu-id="a782e-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a782e-108">EXAMPLES</span></span>

### <span data-ttu-id="a782e-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a782e-109">Example 1</span></span>
```powershell
PS C:\> $aznsActionGroup = New-AzScheduledQueryRuleAznsActionGroup -ActionGroup @("/subscriptions/ad825170-845c-47db-8f00-11978947b089/resourcegroups/MyResourceGroup/providers/microsoft.insights/actiongroups/MyActionGroup") -EmailSubject "Email subject" -CustomWebhookPayload "{}"
```

## <span data-ttu-id="a782e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a782e-110">PARAMETERS</span></span>

### <span data-ttu-id="a782e-111">-ActionGroup</span><span class="sxs-lookup"><span data-stu-id="a782e-111">-ActionGroup</span></span>
<span data-ttu-id="a782e-112">Bildirim gönderilecek eylem gruplarının listesi</span><span class="sxs-lookup"><span data-stu-id="a782e-112">The list of action groups to send notification to</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a782e-113">-Customweb, yük</span><span class="sxs-lookup"><span data-stu-id="a782e-113">-CustomWebhookPayload</span></span>
<span data-ttu-id="a782e-114">Özelleştirilmiş Web kancası yükü</span><span class="sxs-lookup"><span data-stu-id="a782e-114">The customized webhook payload</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a782e-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a782e-115">-DefaultProfile</span></span>
<span data-ttu-id="a782e-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a782e-116">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a782e-117">-EmailSubject</span><span class="sxs-lookup"><span data-stu-id="a782e-117">-EmailSubject</span></span>
<span data-ttu-id="a782e-118">Uyarı bildiriminin e-posta konusu</span><span class="sxs-lookup"><span data-stu-id="a782e-118">The email subject of alert notification</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a782e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a782e-119">CommonParameters</span></span>
<span data-ttu-id="a782e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a782e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a782e-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a782e-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a782e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a782e-122">INPUTS</span></span>

### <span data-ttu-id="a782e-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a782e-123">None</span></span>

## <span data-ttu-id="a782e-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a782e-124">OUTPUTS</span></span>

### <span data-ttu-id="a782e-125">Microsoft. Azure. Commands. Insights. OutputClasses. PSScheduledQueryRuleAznsAction</span><span class="sxs-lookup"><span data-stu-id="a782e-125">Microsoft.Azure.Commands.Insights.OutputClasses.PSScheduledQueryRuleAznsAction</span></span>

## <span data-ttu-id="a782e-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a782e-126">NOTES</span></span>

## <span data-ttu-id="a782e-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a782e-127">RELATED LINKS</span></span>

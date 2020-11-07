---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 2fc67e4f50d3c0a045ed6f0e6d82d5bf46d10c25
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592622"
---
# <span data-ttu-id="7fbd8-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="7fbd8-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="7fbd8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7fbd8-102">SYNOPSIS</span></span>
<span data-ttu-id="7fbd8-103">Otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7fbd8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7fbd8-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Properties] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7fbd8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7fbd8-105">DESCRIPTION</span></span>
<span data-ttu-id="7fbd8-106">**Yeni-Azurermautoscaleweb** kancası cmdlet 'ı bir otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="7fbd8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7fbd8-107">EXAMPLES</span></span>

## <span data-ttu-id="7fbd8-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7fbd8-108">PARAMETERS</span></span>

### <span data-ttu-id="7fbd8-109">-Özellikler</span><span class="sxs-lookup"><span data-stu-id="7fbd8-109">-Properties</span></span>
<span data-ttu-id="7fbd8-110">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-110">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: 

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbd8-111">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="7fbd8-111">-ServiceUri</span></span>
<span data-ttu-id="7fbd8-112">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-112">Specifies the service URI.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7fbd8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7fbd8-113">-DefaultProfile</span></span>
<span data-ttu-id="7fbd8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7fbd8-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7fbd8-115">CommonParameters</span></span>
<span data-ttu-id="7fbd8-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7fbd8-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7fbd8-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7fbd8-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7fbd8-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7fbd8-118">INPUTS</span></span>

## <span data-ttu-id="7fbd8-119">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7fbd8-119">OUTPUTS</span></span>

### <span data-ttu-id="7fbd8-120">Microsoft. Azure. Management. Monitor. Management. modeller. Web, Notification</span><span class="sxs-lookup"><span data-stu-id="7fbd8-120">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="7fbd8-121">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7fbd8-121">NOTES</span></span>

## <span data-ttu-id="7fbd8-122">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7fbd8-122">RELATED LINKS</span></span>

[<span data-ttu-id="7fbd8-123">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="7fbd8-123">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)


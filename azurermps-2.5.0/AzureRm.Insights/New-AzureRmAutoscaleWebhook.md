---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
ms.openlocfilehash: fe6170842bcacf4d7fb0c8e442dc988c03c67e35
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93939386"
---
# <span data-ttu-id="f6f0d-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="f6f0d-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="f6f0d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f6f0d-102">SYNOPSIS</span></span>
<span data-ttu-id="f6f0d-103">Otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6f0d-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f6f0d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f6f0d-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f6f0d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f6f0d-105">DESCRIPTION</span></span>
<span data-ttu-id="f6f0d-106">**Yeni-Azurermautoscaleweb** kancası cmdlet 'ı bir otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f6f0d-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="f6f0d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f6f0d-107">EXAMPLES</span></span>

## <span data-ttu-id="f6f0d-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f6f0d-108">PARAMETERS</span></span>

### <span data-ttu-id="f6f0d-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f6f0d-109">-DefaultProfile</span></span>
<span data-ttu-id="f6f0d-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f6f0d-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f6f0d-111">-Özellik</span><span class="sxs-lookup"><span data-stu-id="f6f0d-111">-Property</span></span>
<span data-ttu-id="f6f0d-112">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f0d-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="f6f0d-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="f6f0d-113">-ServiceUri</span></span>
<span data-ttu-id="f6f0d-114">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="f6f0d-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="f6f0d-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f6f0d-115">CommonParameters</span></span>
<span data-ttu-id="f6f0d-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f6f0d-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f6f0d-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f6f0d-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f6f0d-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f6f0d-118">INPUTS</span></span>

### <span data-ttu-id="f6f0d-119">System. String</span><span class="sxs-lookup"><span data-stu-id="f6f0d-119">System.String</span></span>

### <span data-ttu-id="f6f0d-120">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="f6f0d-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="f6f0d-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f6f0d-121">OUTPUTS</span></span>

### <span data-ttu-id="f6f0d-122">Microsoft. Azure. Management. Monitor. Management. modeller. Web, Notification</span><span class="sxs-lookup"><span data-stu-id="f6f0d-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="f6f0d-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f6f0d-123">NOTES</span></span>

## <span data-ttu-id="f6f0d-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f6f0d-124">RELATED LINKS</span></span>

[<span data-ttu-id="f6f0d-125">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="f6f0d-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



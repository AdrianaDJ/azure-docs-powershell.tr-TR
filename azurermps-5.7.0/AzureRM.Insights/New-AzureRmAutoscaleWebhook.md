---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmAutoscaleWebhook.md
ms.openlocfilehash: 8b94ad5728e7852bb3cd834e7479a29cc11c1698
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93592496"
---
# <span data-ttu-id="3b9d6-101">New-AzureRmAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="3b9d6-101">New-AzureRmAutoscaleWebhook</span></span>

## <span data-ttu-id="3b9d6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b9d6-102">SYNOPSIS</span></span>
<span data-ttu-id="3b9d6-103">Otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-103">Creates an Autoscale webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="3b9d6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b9d6-104">SYNTAX</span></span>

```
New-AzureRmAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="3b9d6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b9d6-105">DESCRIPTION</span></span>
<span data-ttu-id="3b9d6-106">**Yeni-Azurermautoscaleweb** kancası cmdlet 'ı bir otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-106">The **New-AzureRmAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="3b9d6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b9d6-107">EXAMPLES</span></span>

## <span data-ttu-id="3b9d6-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b9d6-108">PARAMETERS</span></span>

### <span data-ttu-id="3b9d6-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b9d6-109">-DefaultProfile</span></span>
<span data-ttu-id="3b9d6-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="3b9d6-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d6-111">-Özellik</span><span class="sxs-lookup"><span data-stu-id="3b9d6-111">-Property</span></span>
<span data-ttu-id="3b9d6-112">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Properties

Required: False
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d6-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="3b9d6-113">-ServiceUri</span></span>
<span data-ttu-id="3b9d6-114">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-114">Specifies the service URI.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b9d6-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b9d6-115">CommonParameters</span></span>
<span data-ttu-id="3b9d6-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b9d6-117">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="3b9d6-117">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b9d6-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b9d6-118">INPUTS</span></span>

### <span data-ttu-id="3b9d6-119">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="3b9d6-119">None</span></span>
<span data-ttu-id="3b9d6-120">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="3b9d6-120">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="3b9d6-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d6-121">OUTPUTS</span></span>

### <span data-ttu-id="3b9d6-122">Microsoft. Azure. Management. Monitor. Management. modeller. Web, Notification</span><span class="sxs-lookup"><span data-stu-id="3b9d6-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="3b9d6-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b9d6-123">NOTES</span></span>

## <span data-ttu-id="3b9d6-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b9d6-124">RELATED LINKS</span></span>

[<span data-ttu-id="3b9d6-125">Yeni-Azurermalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="3b9d6-125">New-AzureRmAlertRuleWebhook</span></span>](./New-AzureRmAlertRuleWebhook.md)



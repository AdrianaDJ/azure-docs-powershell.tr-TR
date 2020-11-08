---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 674A11E4-36B9-4075-9F4E-952BD9FF07A7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/new-azautoscalewebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/New-AzAutoscaleWebhook.md
ms.openlocfilehash: f9e9d9bea69944fdd6eae6c81a4472dee1816e4e
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096299"
---
# <span data-ttu-id="8bfcb-101">New-AzAutoscaleWebhook</span><span class="sxs-lookup"><span data-stu-id="8bfcb-101">New-AzAutoscaleWebhook</span></span>

## <span data-ttu-id="8bfcb-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="8bfcb-102">SYNOPSIS</span></span>
<span data-ttu-id="8bfcb-103">Otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-103">Creates an Autoscale webhook.</span></span>

## <span data-ttu-id="8bfcb-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="8bfcb-104">SYNTAX</span></span>

```
New-AzAutoscaleWebhook [-ServiceUri] <String> [[-Property] <Hashtable>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="8bfcb-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="8bfcb-105">DESCRIPTION</span></span>
<span data-ttu-id="8bfcb-106">**Yeni-Azautoscaleweb kancası** cmdlet 'ı otomatik ölçeklendirme Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-106">The **New-AzAutoscaleWebhook** cmdlet creates an Autoscale webhook.</span></span>

## <span data-ttu-id="8bfcb-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="8bfcb-107">EXAMPLES</span></span>

## <span data-ttu-id="8bfcb-108">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="8bfcb-108">PARAMETERS</span></span>

### <span data-ttu-id="8bfcb-109">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="8bfcb-109">-DefaultProfile</span></span>
<span data-ttu-id="8bfcb-110">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="8bfcb-110">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="8bfcb-111">-Özellik</span><span class="sxs-lookup"><span data-stu-id="8bfcb-111">-Property</span></span>
<span data-ttu-id="8bfcb-112">@ (Property1 = ' değer1 ',....) biçimindeki özelliklerin listesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-112">Specifies the list of properties in the format @(property1 = 'value1',....).</span></span>

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

### <span data-ttu-id="8bfcb-113">-ServiceUri</span><span class="sxs-lookup"><span data-stu-id="8bfcb-113">-ServiceUri</span></span>
<span data-ttu-id="8bfcb-114">Hizmet URI 'sini belirtir.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-114">Specifies the service URI.</span></span>

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

### <span data-ttu-id="8bfcb-115">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="8bfcb-115">CommonParameters</span></span>
<span data-ttu-id="8bfcb-116">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-116">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="8bfcb-117">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="8bfcb-117">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="8bfcb-118">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="8bfcb-118">INPUTS</span></span>

### <span data-ttu-id="8bfcb-119">System. String</span><span class="sxs-lookup"><span data-stu-id="8bfcb-119">System.String</span></span>

### <span data-ttu-id="8bfcb-120">System. topluluklar. Hashtable</span><span class="sxs-lookup"><span data-stu-id="8bfcb-120">System.Collections.Hashtable</span></span>

## <span data-ttu-id="8bfcb-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="8bfcb-121">OUTPUTS</span></span>

### <span data-ttu-id="8bfcb-122">Microsoft. Azure. Management. Monitor. Management. modeller. Web, Notification</span><span class="sxs-lookup"><span data-stu-id="8bfcb-122">Microsoft.Azure.Management.Monitor.Management.Models.WebhookNotification</span></span>

## <span data-ttu-id="8bfcb-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="8bfcb-123">NOTES</span></span>

## <span data-ttu-id="8bfcb-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="8bfcb-124">RELATED LINKS</span></span>

[<span data-ttu-id="8bfcb-125">Yeni-Azalertruleweb kancası</span><span class="sxs-lookup"><span data-stu-id="8bfcb-125">New-AzAlertRuleWebhook</span></span>](./New-AzAlertRuleWebhook.md)



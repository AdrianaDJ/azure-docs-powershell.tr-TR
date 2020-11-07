---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: 9428ea3c297bcdab01ee6464d38b5c20910b69d1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762644"
---
# <span data-ttu-id="cd7f3-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd7f3-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="cd7f3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="cd7f3-102">SYNOPSIS</span></span>
<span data-ttu-id="cd7f3-103">Bellekte bir ActionGroup başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="cd7f3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="cd7f3-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="cd7f3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="cd7f3-105">DESCRIPTION</span></span>
<span data-ttu-id="cd7f3-106">**Yeni-AzureRmActionGroup** cmdlet 'i bellekte bir eylem grubu başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="cd7f3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="cd7f3-107">EXAMPLES</span></span>

### <span data-ttu-id="cd7f3-108">Örnek 1: bellekte eylem grubu başvuru nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="cd7f3-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="cd7f3-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="cd7f3-109">PARAMETERS</span></span>

### <span data-ttu-id="cd7f3-110">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="cd7f3-110">-ActionGroupId</span></span>
<span data-ttu-id="cd7f3-111">Eylem grubunun kimliği/adı.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-111">The Id/name of the action group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="cd7f3-112">-DefaultProfile</span></span>
<span data-ttu-id="cd7f3-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="cd7f3-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="cd7f3-114">-Web, Özellik</span><span class="sxs-lookup"><span data-stu-id="cd7f3-114">-WebhookProperty</span></span>
<span data-ttu-id="cd7f3-115">Eylem grubunun Web kancası özellikleri</span><span class="sxs-lookup"><span data-stu-id="cd7f3-115">The webhook properties of the action group</span></span>

```yaml
Type: System.Collections.Generic.Dictionary`2[System.String,System.String]
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="cd7f3-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="cd7f3-116">CommonParameters</span></span>
<span data-ttu-id="cd7f3-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="cd7f3-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="cd7f3-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="cd7f3-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="cd7f3-119">INPUTS</span></span>

### <span data-ttu-id="cd7f3-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="cd7f3-120">None</span></span>
<span data-ttu-id="cd7f3-121">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="cd7f3-121">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="cd7f3-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="cd7f3-122">OUTPUTS</span></span>

### <span data-ttu-id="cd7f3-123">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="cd7f3-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="cd7f3-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="cd7f3-124">NOTES</span></span>

## <span data-ttu-id="cd7f3-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="cd7f3-125">RELATED LINKS</span></span>

[<span data-ttu-id="cd7f3-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cd7f3-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cd7f3-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cd7f3-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cd7f3-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cd7f3-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cd7f3-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cd7f3-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cd7f3-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="cd7f3-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="cd7f3-131">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="cd7f3-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/New-AzureRmActionGroup.md
ms.openlocfilehash: d4afe709d70872c1d7fb59e99f2f98d3dfe19d6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93763375"
---
# <span data-ttu-id="98d13-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="98d13-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="98d13-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="98d13-102">SYNOPSIS</span></span>
<span data-ttu-id="98d13-103">Bellekte bir ActionGroup başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98d13-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="98d13-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="98d13-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="98d13-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="98d13-105">DESCRIPTION</span></span>
<span data-ttu-id="98d13-106">**Yeni-AzureRmActionGroup** cmdlet 'i bellekte bir eylem grubu başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="98d13-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="98d13-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="98d13-107">EXAMPLES</span></span>

### <span data-ttu-id="98d13-108">Örnek 1: bellekte eylem grubu başvuru nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="98d13-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="98d13-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="98d13-109">PARAMETERS</span></span>

### <span data-ttu-id="98d13-110">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="98d13-110">-ActionGroupId</span></span>
<span data-ttu-id="98d13-111">Eylem grubunun kimliği/adı.</span><span class="sxs-lookup"><span data-stu-id="98d13-111">The Id/name of the action group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="98d13-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="98d13-112">-DefaultProfile</span></span>
<span data-ttu-id="98d13-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="98d13-113">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="98d13-114">-Web, Özellik</span><span class="sxs-lookup"><span data-stu-id="98d13-114">-WebhookProperty</span></span>
<span data-ttu-id="98d13-115">Eylem grubunun Web kancası özellikleri</span><span class="sxs-lookup"><span data-stu-id="98d13-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="98d13-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="98d13-116">CommonParameters</span></span>
<span data-ttu-id="98d13-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="98d13-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="98d13-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="98d13-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="98d13-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="98d13-119">INPUTS</span></span>

## <span data-ttu-id="98d13-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="98d13-120">OUTPUTS</span></span>

### <span data-ttu-id="98d13-121">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="98d13-121">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="98d13-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="98d13-122">NOTES</span></span>

## <span data-ttu-id="98d13-123">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="98d13-123">RELATED LINKS</span></span>

[<span data-ttu-id="98d13-124">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98d13-124">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="98d13-125">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98d13-125">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="98d13-126">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98d13-126">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="98d13-127">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98d13-127">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="98d13-128">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="98d13-128">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="98d13-129">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="98d13-129">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


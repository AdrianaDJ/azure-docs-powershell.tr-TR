---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A4C605DD-9B2E-4EE9-BD1F-1352D605C33F
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/new-azurermactiongroup
schema: 2.0.0
ms.openlocfilehash: b2f9738518f446b9cf5bfbefe0c7025bb3351628
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93938868"
---
# <span data-ttu-id="f555d-101">New-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="f555d-101">New-AzureRmActionGroup</span></span>

## <span data-ttu-id="f555d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f555d-102">SYNOPSIS</span></span>
<span data-ttu-id="f555d-103">Bellekte bir ActionGroup başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f555d-103">Creates an ActionGroup reference object in memory.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f555d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f555d-104">SYNTAX</span></span>

```
New-AzureRmActionGroup -ActionGroupId <String>
 [-WebhookProperty <System.Collections.Generic.Dictionary`2[System.String,System.String]>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f555d-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f555d-105">DESCRIPTION</span></span>
<span data-ttu-id="f555d-106">**Yeni-AzureRmActionGroup** cmdlet 'i bellekte bir eylem grubu başvuru nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f555d-106">The **New-AzureRmActionGroup** cmdlet creates an action group reference object in memory.</span></span>

## <span data-ttu-id="f555d-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f555d-107">EXAMPLES</span></span>

### <span data-ttu-id="f555d-108">Örnek 1: bellekte eylem grubu başvuru nesnesi oluşturma</span><span class="sxs-lookup"><span data-stu-id="f555d-108">Example 1: Create an action group reference object in memory</span></span>
```
PS C:\>$dict = New-Object "System.Collections.Generic.Dictionary``2[System.String,System.String]"
PS C:\>$dict.Add('key1', 'value1')
PS C:\>$actionGrp1 = New-AzureRmActionGroup -ActionGroupId 'actiongr1' -WebhookProperties $dict
```

## <span data-ttu-id="f555d-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f555d-109">PARAMETERS</span></span>

### <span data-ttu-id="f555d-110">-Actiongroupıd</span><span class="sxs-lookup"><span data-stu-id="f555d-110">-ActionGroupId</span></span>
<span data-ttu-id="f555d-111">Eylem grubunun kimliği/adı.</span><span class="sxs-lookup"><span data-stu-id="f555d-111">The Id/name of the action group.</span></span>

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

### <span data-ttu-id="f555d-112">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f555d-112">-DefaultProfile</span></span>
<span data-ttu-id="f555d-113">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="f555d-113">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="f555d-114">-Web, Özellik</span><span class="sxs-lookup"><span data-stu-id="f555d-114">-WebhookProperty</span></span>
<span data-ttu-id="f555d-115">Eylem grubunun Web kancası özellikleri</span><span class="sxs-lookup"><span data-stu-id="f555d-115">The webhook properties of the action group</span></span>

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

### <span data-ttu-id="f555d-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f555d-116">CommonParameters</span></span>
<span data-ttu-id="f555d-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f555d-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f555d-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f555d-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f555d-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f555d-119">INPUTS</span></span>

### <span data-ttu-id="f555d-120">System. String</span><span class="sxs-lookup"><span data-stu-id="f555d-120">System.String</span></span>

### <span data-ttu-id="f555d-121">System. Koleksiyonlar. Generic. Dictionary ' 2 [[System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089], [System. String, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="f555d-121">System.Collections.Generic.Dictionary\`2[[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089],[System.String, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="f555d-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f555d-122">OUTPUTS</span></span>

### <span data-ttu-id="f555d-123">Microsoft. Azure. Management. Monitor. Management. modeller. ActivityLogAlertActionGroup</span><span class="sxs-lookup"><span data-stu-id="f555d-123">Microsoft.Azure.Management.Monitor.Management.Models.ActivityLogAlertActionGroup</span></span>

## <span data-ttu-id="f555d-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f555d-124">NOTES</span></span>

## <span data-ttu-id="f555d-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f555d-125">RELATED LINKS</span></span>

[<span data-ttu-id="f555d-126">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f555d-126">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f555d-127">Enable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f555d-127">Enable-AzureRmActivityLogAlert</span></span>](./Enable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f555d-128">Disable-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f555d-128">Disable-AzureRmActivityLogAlert</span></span>](./Disable-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f555d-129">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f555d-129">Get-AzureRmActivityLogAlert</span></span>](./Get-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f555d-130">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="f555d-130">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="f555d-131">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="f555d-131">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)


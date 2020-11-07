---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 92550ee9f5eed7cf31624748140a0355ac6849ec
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764402"
---
# <span data-ttu-id="c5dee-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5dee-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="c5dee-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c5dee-102">SYNOPSIS</span></span>
<span data-ttu-id="c5dee-103">Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="c5dee-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c5dee-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c5dee-104">SYNTAX</span></span>

### <span data-ttu-id="c5dee-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="c5dee-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c5dee-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="c5dee-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="c5dee-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="c5dee-107">DESCRIPTION</span></span>
<span data-ttu-id="c5dee-108">**Get-AzureRmActivityLogAlert** cmdlet 'i, bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="c5dee-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="c5dee-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c5dee-109">EXAMPLES</span></span>

### <span data-ttu-id="c5dee-110">Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="c5dee-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="c5dee-111">Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5dee-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="c5dee-112">Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="c5dee-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="c5dee-113">Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5dee-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="c5dee-114">Örnek 3: etkinlik günlüğü uyarısı alın.</span><span class="sxs-lookup"><span data-stu-id="c5dee-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="c5dee-115">Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.</span><span class="sxs-lookup"><span data-stu-id="c5dee-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="c5dee-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c5dee-116">PARAMETERS</span></span>

### <span data-ttu-id="c5dee-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c5dee-117">-DefaultProfile</span></span>
<span data-ttu-id="c5dee-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c5dee-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c5dee-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="c5dee-119">-Name</span></span>
<span data-ttu-id="c5dee-120">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="c5dee-120">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5dee-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c5dee-121">-ResourceGroupName</span></span>
<span data-ttu-id="c5dee-122">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="c5dee-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="c5dee-123">Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="c5dee-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByNameAndResourceGroup
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: GetByResourceGroup
Aliases:

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c5dee-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c5dee-124">CommonParameters</span></span>
<span data-ttu-id="c5dee-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c5dee-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c5dee-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c5dee-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c5dee-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c5dee-127">INPUTS</span></span>

### <span data-ttu-id="c5dee-128">System. String</span><span class="sxs-lookup"><span data-stu-id="c5dee-128">System.String</span></span>

## <span data-ttu-id="c5dee-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c5dee-129">OUTPUTS</span></span>

### <span data-ttu-id="c5dee-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="c5dee-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="c5dee-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c5dee-131">NOTES</span></span>

## <span data-ttu-id="c5dee-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c5dee-132">RELATED LINKS</span></span>

[<span data-ttu-id="c5dee-133">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5dee-133">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5dee-134">Güncelleştirme-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5dee-134">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5dee-135">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="c5dee-135">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="c5dee-136">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="c5dee-136">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="c5dee-137">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="c5dee-137">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

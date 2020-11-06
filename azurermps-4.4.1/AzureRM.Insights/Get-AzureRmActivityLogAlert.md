---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: b4a1204d25852aa75c7b68c90305aefe9cfefe6c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594671"
---
# <span data-ttu-id="0af43-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0af43-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="0af43-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0af43-102">SYNOPSIS</span></span>
<span data-ttu-id="0af43-103">Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0af43-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0af43-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0af43-104">SYNTAX</span></span>

### <span data-ttu-id="0af43-105">Etkinlik günlüğü uyarısı alma uyarısı</span><span class="sxs-lookup"><span data-stu-id="0af43-105">Default parameters for get an activity log alert</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="0af43-106">Ad verildiğinde kaynak grubun verildiğinden emin olmak için parametreler</span><span class="sxs-lookup"><span data-stu-id="0af43-106">Parameters to make sure the resource group is given when the name is given</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="0af43-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="0af43-107">DESCRIPTION</span></span>
<span data-ttu-id="0af43-108">**Get-AzureRmActivityLogAlert** cmdlet 'i, bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="0af43-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="0af43-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0af43-109">EXAMPLES</span></span>

### <span data-ttu-id="0af43-110">Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="0af43-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="0af43-111">Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0af43-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="0af43-112">Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="0af43-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="0af43-113">Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0af43-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="0af43-114">Örnek 3: etkinlik günlüğü uyarısı alın.</span><span class="sxs-lookup"><span data-stu-id="0af43-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="0af43-115">Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.</span><span class="sxs-lookup"><span data-stu-id="0af43-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="0af43-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0af43-116">PARAMETERS</span></span>

### <span data-ttu-id="0af43-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="0af43-117">-Name</span></span>
<span data-ttu-id="0af43-118">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="0af43-118">The name of the activity log alert.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af43-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0af43-119">-ResourceGroupName</span></span>
<span data-ttu-id="0af43-120">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0af43-120">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="0af43-121">Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="0af43-121">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: System.String
Parameter Sets: Default parameters for get an activity log alert
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Parameters to make sure the resource group is given when the name is given
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="0af43-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0af43-122">-DefaultProfile</span></span>
<span data-ttu-id="0af43-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0af43-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0af43-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0af43-124">CommonParameters</span></span>
<span data-ttu-id="0af43-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0af43-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0af43-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0af43-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0af43-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0af43-127">INPUTS</span></span>

### <span data-ttu-id="0af43-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0af43-128">None</span></span>

## <span data-ttu-id="0af43-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0af43-129">OUTPUTS</span></span>

### <span data-ttu-id="0af43-130"><System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="0af43-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="0af43-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="0af43-131">None</span></span>

## <span data-ttu-id="0af43-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0af43-132">NOTES</span></span>

## <span data-ttu-id="0af43-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0af43-133">RELATED LINKS</span></span>

[<span data-ttu-id="0af43-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0af43-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="0af43-135">Güncelleştirme-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0af43-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="0af43-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="0af43-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="0af43-137">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="0af43-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="0af43-138">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="0af43-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

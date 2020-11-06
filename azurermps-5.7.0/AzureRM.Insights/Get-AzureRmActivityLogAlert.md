---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmActivityLogAlert.md
ms.openlocfilehash: 41ed224333d9d0ab1aa542629f46fcf6d8db5fc4
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594474"
---
# <span data-ttu-id="50f55-101">Get-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50f55-101">Get-AzureRmActivityLogAlert</span></span>

## <span data-ttu-id="50f55-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="50f55-102">SYNOPSIS</span></span>
<span data-ttu-id="50f55-103">Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="50f55-103">Gets one or more activity log alert resources.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="50f55-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="50f55-104">SYNTAX</span></span>

### <span data-ttu-id="50f55-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="50f55-105">GetByNameAndResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert -ResourceGroupName <String> -Name <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="50f55-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="50f55-106">GetByResourceGroup</span></span>
```
Get-AzureRmActivityLogAlert [-ResourceGroupName <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="50f55-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="50f55-107">DESCRIPTION</span></span>
<span data-ttu-id="50f55-108">**Get-AzureRmActivityLogAlert** cmdlet 'i, bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="50f55-108">The **Get-AzureRmActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="50f55-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="50f55-109">EXAMPLES</span></span>

### <span data-ttu-id="50f55-110">Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="50f55-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert
```

<span data-ttu-id="50f55-111">Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="50f55-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="50f55-112">Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="50f55-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="50f55-113">Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="50f55-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="50f55-114">Örnek 3: etkinlik günlüğü uyarısı alın.</span><span class="sxs-lookup"><span data-stu-id="50f55-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzureRmActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="50f55-115">Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.</span><span class="sxs-lookup"><span data-stu-id="50f55-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="50f55-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="50f55-116">PARAMETERS</span></span>

### <span data-ttu-id="50f55-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="50f55-117">-DefaultProfile</span></span>
<span data-ttu-id="50f55-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="50f55-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="50f55-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="50f55-119">-Name</span></span>
<span data-ttu-id="50f55-120">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="50f55-120">The name of the activity log alert.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f55-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="50f55-121">-ResourceGroupName</span></span>
<span data-ttu-id="50f55-122">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="50f55-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="50f55-123">Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="50f55-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

```yaml
Type: String
Parameter Sets: GetByNameAndResourceGroup
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: String
Parameter Sets: GetByResourceGroup
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="50f55-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="50f55-124">CommonParameters</span></span>
<span data-ttu-id="50f55-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="50f55-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="50f55-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="50f55-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="50f55-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="50f55-127">INPUTS</span></span>

### <span data-ttu-id="50f55-128">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50f55-128">None</span></span>

## <span data-ttu-id="50f55-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="50f55-129">OUTPUTS</span></span>

### <span data-ttu-id="50f55-130"><System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource]</span><span class="sxs-lookup"><span data-stu-id="50f55-130"><System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource]</span></span>

### <span data-ttu-id="50f55-131">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="50f55-131">None</span></span>

## <span data-ttu-id="50f55-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="50f55-132">NOTES</span></span>

## <span data-ttu-id="50f55-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="50f55-133">RELATED LINKS</span></span>

[<span data-ttu-id="50f55-134">Set-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50f55-134">Set-AzureRmActivityLogAlert</span></span>](./Set-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50f55-135">Güncelleştirme-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50f55-135">Update-AzureRmActivityLogAlert</span></span>](./Update-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50f55-136">Remove-AzureRmActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="50f55-136">Remove-AzureRmActivityLogAlert</span></span>](./Remove-AzureRmActivityLogAlert.md)

[<span data-ttu-id="50f55-137">Yeni-AzureRmActionGroup</span><span class="sxs-lookup"><span data-stu-id="50f55-137">New-AzureRmActionGroup</span></span>](./New-AzureRmActionGroup.md)

[<span data-ttu-id="50f55-138">Yeni-AzureRmActivityLogAlertCondition</span><span class="sxs-lookup"><span data-stu-id="50f55-138">New-AzureRmActivityLogAlertCondition</span></span>](./Get-AzureRmActivityLogAlertCondition.md)

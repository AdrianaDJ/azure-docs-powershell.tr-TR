---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: 85492E00-3776-4F20-A444-9C28CC6154B7
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azactivitylogalert
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Monitor/Monitor/help/Get-AzActivityLogAlert.md
ms.openlocfilehash: 030564f700f399b1880d36e4dac628a9fc3efa35
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94274445"
---
# <span data-ttu-id="2cef5-101">Get-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2cef5-101">Get-AzActivityLogAlert</span></span>

## <span data-ttu-id="2cef5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2cef5-102">SYNOPSIS</span></span>
<span data-ttu-id="2cef5-103">Bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="2cef5-103">Gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2cef5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2cef5-104">SYNTAX</span></span>

### <span data-ttu-id="2cef5-105">Getbynaik Vseçresourcegroup</span><span class="sxs-lookup"><span data-stu-id="2cef5-105">GetByNameAndResourceGroup</span></span>
```
Get-AzActivityLogAlert [-ResourceGroupName] <String> [-Name] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2cef5-106">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="2cef5-106">GetByResourceGroup</span></span>
```
Get-AzActivityLogAlert [[-ResourceGroupName] <String>] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="2cef5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="2cef5-107">DESCRIPTION</span></span>
<span data-ttu-id="2cef5-108">**Get-Azactivilogalert** cmdlet 'i bir veya daha fazla etkinlik günlüğü uyarı kaynağını alır.</span><span class="sxs-lookup"><span data-stu-id="2cef5-108">The **Get-AzActivityLogAlert** cmdlet gets one or more activity log alert resources.</span></span>

## <span data-ttu-id="2cef5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2cef5-109">EXAMPLES</span></span>

### <span data-ttu-id="2cef5-110">Örnek 1: abonelik KIMLIĞINE göre etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="2cef5-110">Example 1: Get a activity log alerts by subscription ID</span></span>
```
PS C:\>Get-AzActivityLogAlert
```

<span data-ttu-id="2cef5-111">Bu komut, geçerli aboneliğin tüm etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="2cef5-111">This command lists all the activity log alerts for the current subscription.</span></span>

### <span data-ttu-id="2cef5-112">Örnek 2: verilen kaynak grubu için etkinlik günlüğü uyarılarını alma</span><span class="sxs-lookup"><span data-stu-id="2cef5-112">Example 2: Get activity log alerts for the given resource group</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts"
```

<span data-ttu-id="2cef5-113">Bu komut, verilen kaynak grubunun etkinlik günlüğü uyarılarını listeler.</span><span class="sxs-lookup"><span data-stu-id="2cef5-113">This command lists activity log alerts for the given resource group.</span></span>

### <span data-ttu-id="2cef5-114">Örnek 3: etkinlik günlüğü uyarısı alın.</span><span class="sxs-lookup"><span data-stu-id="2cef5-114">Example 3: Get an activity log alert.</span></span>
```
PS C:\>Get-AzActivityLogAlert -ResourceGroupName "Default-activityLogAlerts" -Name "alert1"
```

<span data-ttu-id="2cef5-115">Bu komut, bir (tek öğe içeren bir liste) etkinlik günlüğü uyarısını listeler.</span><span class="sxs-lookup"><span data-stu-id="2cef5-115">This command lists one (a list with a single element) activity log alert.</span></span>

## <span data-ttu-id="2cef5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2cef5-116">PARAMETERS</span></span>

### <span data-ttu-id="2cef5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2cef5-117">-DefaultProfile</span></span>
<span data-ttu-id="2cef5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="2cef5-118">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="2cef5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="2cef5-119">-Name</span></span>
<span data-ttu-id="2cef5-120">Etkinlik günlüğü uyarısının adı.</span><span class="sxs-lookup"><span data-stu-id="2cef5-120">The name of the activity log alert.</span></span>

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

### <span data-ttu-id="2cef5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2cef5-121">-ResourceGroupName</span></span>
<span data-ttu-id="2cef5-122">Uyarı kaynağının bulunduğu kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="2cef5-122">The name of the resource group where the alert resource exists.</span></span>
<span data-ttu-id="2cef5-123">Ad null veya boş değilse, bu parametrenin boş dize içermesi ve içermemesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="2cef5-123">If Name is not null or empty, this parameter must contain and non empty string.</span></span>

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

### <span data-ttu-id="2cef5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2cef5-124">CommonParameters</span></span>
<span data-ttu-id="2cef5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2cef5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2cef5-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="2cef5-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2cef5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2cef5-127">INPUTS</span></span>

### <span data-ttu-id="2cef5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="2cef5-128">System.String</span></span>

## <span data-ttu-id="2cef5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2cef5-129">OUTPUTS</span></span>

### <span data-ttu-id="2cef5-130">Microsoft. Azure. Commands. Insights. OutputClasses. PSActivityLogAlertResource</span><span class="sxs-lookup"><span data-stu-id="2cef5-130">Microsoft.Azure.Commands.Insights.OutputClasses.PSActivityLogAlertResource</span></span>

## <span data-ttu-id="2cef5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2cef5-131">NOTES</span></span>

## <span data-ttu-id="2cef5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2cef5-132">RELATED LINKS</span></span>

[<span data-ttu-id="2cef5-133">Set-Azactivilogalert</span><span class="sxs-lookup"><span data-stu-id="2cef5-133">Set-AzActivityLogAlert</span></span>](./Set-AzActivityLogAlert.md)

[<span data-ttu-id="2cef5-134">Update-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2cef5-134">Update-AzActivityLogAlert</span></span>](./Update-AzActivityLogAlert.md)

[<span data-ttu-id="2cef5-135">Remove-AzActivityLogAlert</span><span class="sxs-lookup"><span data-stu-id="2cef5-135">Remove-AzActivityLogAlert</span></span>](./Remove-AzActivityLogAlert.md)

[<span data-ttu-id="2cef5-136">Yeni-AzActionGroup</span><span class="sxs-lookup"><span data-stu-id="2cef5-136">New-AzActionGroup</span></span>](./New-AzActionGroup.md)

[<span data-ttu-id="2cef5-137">Yeni-Azactivilogalertcondition</span><span class="sxs-lookup"><span data-stu-id="2cef5-137">New-AzActivityLogAlertCondition</span></span>](./New-AzActivityLogAlertCondition.md)

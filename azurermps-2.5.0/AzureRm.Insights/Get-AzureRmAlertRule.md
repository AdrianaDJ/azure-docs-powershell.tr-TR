---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
ms.openlocfilehash: fe763bcf6ff4aeeeedb3ff0dcb0c2ebd5c4b45cc
ms.sourcegitcommit: b9b2dea3441d1532a5564ddca3dced45424fe2d6
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/15/2020
ms.locfileid: "93940138"
---
# <span data-ttu-id="a0734-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0734-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="a0734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a0734-102">SYNOPSIS</span></span>
<span data-ttu-id="a0734-103">Uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0734-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a0734-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a0734-104">SYNTAX</span></span>

### <span data-ttu-id="a0734-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="a0734-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="a0734-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="a0734-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="a0734-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="a0734-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a0734-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="a0734-108">DESCRIPTION</span></span>
<span data-ttu-id="a0734-109">**Get-AzureRmAlertRule** cmdlet 'i, adı veya URI 'sini ya da belirtilen bir kaynak grubundaki tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0734-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="a0734-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a0734-110">EXAMPLES</span></span>

### <span data-ttu-id="a0734-111">Örnek 1: kaynak grubu için uyarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="a0734-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="a0734-112">Bu komut, Default-Web-merkezileştirme adlı kaynak grubu için tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="a0734-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="a0734-113">*DetailedOutput* parametresi belirtilmediğinden, çıktı kurallarla ilgili ayrıntıları içermez.</span><span class="sxs-lookup"><span data-stu-id="a0734-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="a0734-114">Örnek 2: ada göre bir uyarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="a0734-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="a0734-115">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="a0734-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="a0734-116">*DetailedOutput* parametresi belirtilmediğinden, çıkış yalnızca uyarı kuralıyla ilgili temel bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="a0734-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="a0734-117">Örnek 3: ayrıntılı çıktıya sahip bir uyarı kuralı adı alın</span><span class="sxs-lookup"><span data-stu-id="a0734-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="a0734-118">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="a0734-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="a0734-119">*DetailedOutput* parametresi belirtilmiştir, böylece çıktı ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="a0734-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="a0734-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a0734-120">PARAMETERS</span></span>

### <span data-ttu-id="a0734-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a0734-121">-DefaultProfile</span></span>
<span data-ttu-id="a0734-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a0734-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a0734-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="a0734-123">-DetailedOutput</span></span>
<span data-ttu-id="a0734-124">Çıktıda tüm ayrıntıları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a0734-124">Displays full details in the output.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0734-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="a0734-125">-Name</span></span>
<span data-ttu-id="a0734-126">Alınacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0734-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByName
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0734-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a0734-127">-ResourceGroupName</span></span>
<span data-ttu-id="a0734-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0734-128">Specifies the name of the resource group.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0734-129">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="a0734-129">-TargetResourceId</span></span>
<span data-ttu-id="a0734-130">Hedef kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a0734-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: GetByResourceUri
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a0734-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a0734-131">CommonParameters</span></span>
<span data-ttu-id="a0734-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a0734-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a0734-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a0734-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a0734-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a0734-134">INPUTS</span></span>

### <span data-ttu-id="a0734-135">System. String</span><span class="sxs-lookup"><span data-stu-id="a0734-135">System.String</span></span>

### <span data-ttu-id="a0734-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="a0734-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="a0734-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a0734-137">OUTPUTS</span></span>

### <span data-ttu-id="a0734-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0734-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="a0734-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a0734-139">NOTES</span></span>

## <span data-ttu-id="a0734-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a0734-140">RELATED LINKS</span></span>



[<span data-ttu-id="a0734-141">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0734-141">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="a0734-142">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0734-142">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="a0734-143">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="a0734-143">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="a0734-144">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="a0734-144">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



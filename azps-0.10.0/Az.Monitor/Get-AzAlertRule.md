---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Monitor.dll-Help.xml
Module Name: Az.Monitor
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/az.monitor/get-azalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Monitor/Monitor/help/Get-AzAlertRule.md
ms.openlocfilehash: 01774d80ce422c1ac0a48df61d44328b6b5b0105
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93935749"
---
# <span data-ttu-id="036bc-101">Get-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="036bc-101">Get-AzAlertRule</span></span>

## <span data-ttu-id="036bc-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="036bc-102">SYNOPSIS</span></span>
<span data-ttu-id="036bc-103">Uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="036bc-103">Gets alert rules.</span></span>

## <span data-ttu-id="036bc-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="036bc-104">SYNTAX</span></span>

### <span data-ttu-id="036bc-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="036bc-105">GetByResourceGroup</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="036bc-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="036bc-106">GetByName</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="036bc-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="036bc-107">GetByResourceUri</span></span>
```
Get-AzAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="036bc-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="036bc-108">DESCRIPTION</span></span>
<span data-ttu-id="036bc-109">**Get-AzAlertRule** cmdlet 'i, adı veya URI 'sini ya da belirtilen bir kaynak grubundaki tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="036bc-109">The **Get-AzAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="036bc-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="036bc-110">EXAMPLES</span></span>

### <span data-ttu-id="036bc-111">Örnek 1: kaynak grubu için uyarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="036bc-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="036bc-112">Bu komut, Default-Web-merkezileştirme adlı kaynak grubu için tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="036bc-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="036bc-113">*DetailedOutput* parametresi belirtilmediğinden, çıktı kurallarla ilgili ayrıntıları içermez.</span><span class="sxs-lookup"><span data-stu-id="036bc-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="036bc-114">Örnek 2: ada göre bir uyarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="036bc-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="036bc-115">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="036bc-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="036bc-116">*DetailedOutput* parametresi belirtilmediğinden, çıkış yalnızca uyarı kuralıyla ilgili temel bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="036bc-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="036bc-117">Örnek 3: ayrıntılı çıktıya sahip bir uyarı kuralı adı alın</span><span class="sxs-lookup"><span data-stu-id="036bc-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="036bc-118">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="036bc-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="036bc-119">*DetailedOutput* parametresi belirtilmiştir, böylece çıktı ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="036bc-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="036bc-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="036bc-120">PARAMETERS</span></span>

### <span data-ttu-id="036bc-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="036bc-121">-DefaultProfile</span></span>
<span data-ttu-id="036bc-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="036bc-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="036bc-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="036bc-123">-DetailedOutput</span></span>
<span data-ttu-id="036bc-124">Çıktıda tüm ayrıntıları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="036bc-124">Displays full details in the output.</span></span>

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

### <span data-ttu-id="036bc-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="036bc-125">-Name</span></span>
<span data-ttu-id="036bc-126">Alınacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="036bc-126">Specifies the name of the alert rule to get.</span></span>

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

### <span data-ttu-id="036bc-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="036bc-127">-ResourceGroupName</span></span>
<span data-ttu-id="036bc-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="036bc-128">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="036bc-129">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="036bc-129">-TargetResourceId</span></span>
<span data-ttu-id="036bc-130">Hedef kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="036bc-130">Specifies the ID of the target resource.</span></span>

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

### <span data-ttu-id="036bc-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="036bc-131">CommonParameters</span></span>
<span data-ttu-id="036bc-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="036bc-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="036bc-133">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="036bc-133">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="036bc-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="036bc-134">INPUTS</span></span>

### <span data-ttu-id="036bc-135">System. String</span><span class="sxs-lookup"><span data-stu-id="036bc-135">System.String</span></span>

### <span data-ttu-id="036bc-136">System. Management. Automation. SwitchParameter</span><span class="sxs-lookup"><span data-stu-id="036bc-136">System.Management.Automation.SwitchParameter</span></span>

## <span data-ttu-id="036bc-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="036bc-137">OUTPUTS</span></span>

### <span data-ttu-id="036bc-138">Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule</span><span class="sxs-lookup"><span data-stu-id="036bc-138">Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule</span></span>

## <span data-ttu-id="036bc-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="036bc-139">NOTES</span></span>

## <span data-ttu-id="036bc-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="036bc-140">RELATED LINKS</span></span>

[<span data-ttu-id="036bc-141">Add-AzLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="036bc-141">Add-AzLogAlertRule</span></span>](./Add-AzLogAlertRule.md)

[<span data-ttu-id="036bc-142">Add-Azmetrik ıalertrule</span><span class="sxs-lookup"><span data-stu-id="036bc-142">Add-AzMetricAlertRule</span></span>](./Add-AzMetricAlertRule.md)

[<span data-ttu-id="036bc-143">Add-AzWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="036bc-143">Add-AzWebtestAlertRule</span></span>](./Add-AzWebtestAlertRule.md)

[<span data-ttu-id="036bc-144">Get-Azalera</span><span class="sxs-lookup"><span data-stu-id="036bc-144">Get-AzAlertHistory</span></span>](./Get-AzAlertHistory.md)

[<span data-ttu-id="036bc-145">Remove-AzAlertRule</span><span class="sxs-lookup"><span data-stu-id="036bc-145">Remove-AzAlertRule</span></span>](./Remove-AzAlertRule.md)



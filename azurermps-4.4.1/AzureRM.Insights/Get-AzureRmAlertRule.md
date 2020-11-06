---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 65c5bc7a2767fd00497b487783c4e6f0ce6d6723
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594666"
---
# <span data-ttu-id="987ce-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="987ce-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="987ce-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="987ce-102">SYNOPSIS</span></span>
<span data-ttu-id="987ce-103">Uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="987ce-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="987ce-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="987ce-104">SYNTAX</span></span>

### <span data-ttu-id="987ce-105">Get-AzureRmAlertRule cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="987ce-105">Parameters for Get-AzureRmAlertRule cmdlet</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="987ce-106">Ad kullanan Get-AzureRmAlertRule cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="987ce-106">Parameters for Get-AzureRmAlertRule cmdlet using name</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -Name <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="987ce-107">Hedef kaynak URI 'sini kullanarak Get-AzureRmAlertRule cmdlet parametreleri</span><span class="sxs-lookup"><span data-stu-id="987ce-107">Parameters for Get-AzureRmAlertRule cmdlet using target resource uri</span></span>
```
Get-AzureRmAlertRule -ResourceGroup <String> -TargetResourceId <String> [-DetailedOutput]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="987ce-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="987ce-108">DESCRIPTION</span></span>
<span data-ttu-id="987ce-109">**Get-AzureRmAlertRule** cmdlet 'i, adı veya URI 'sini ya da belirtilen bir kaynak grubundaki tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="987ce-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="987ce-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="987ce-110">EXAMPLES</span></span>

### <span data-ttu-id="987ce-111">Örnek 1: kaynak grubu için uyarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="987ce-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="987ce-112">Bu komut, Default-Web-merkezileştirme adlı kaynak grubu için tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="987ce-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="987ce-113">*DetailedOutput* parametresi belirtilmediğinden, çıktı kurallarla ilgili ayrıntıları içermez.</span><span class="sxs-lookup"><span data-stu-id="987ce-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="987ce-114">Örnek 2: ada göre bir uyarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="987ce-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="987ce-115">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="987ce-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="987ce-116">*DetailedOutput* parametresi belirtilmediğinden, çıkış yalnızca uyarı kuralıyla ilgili temel bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="987ce-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="987ce-117">Örnek 3: ayrıntılı çıktıya sahip bir uyarı kuralı adı alın</span><span class="sxs-lookup"><span data-stu-id="987ce-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="987ce-118">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="987ce-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="987ce-119">*DetailedOutput* parametresi belirtilmiştir, böylece çıktı ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="987ce-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="987ce-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="987ce-120">PARAMETERS</span></span>

### <span data-ttu-id="987ce-121">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="987ce-121">-DetailedOutput</span></span>
<span data-ttu-id="987ce-122">Çıktıda tüm ayrıntıları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="987ce-122">Displays full details in the output.</span></span>

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

### <span data-ttu-id="987ce-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="987ce-123">-Name</span></span>
<span data-ttu-id="987ce-124">Alınacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="987ce-124">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using name
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987ce-125">-ResourceGroup</span><span class="sxs-lookup"><span data-stu-id="987ce-125">-ResourceGroup</span></span>
<span data-ttu-id="987ce-126">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="987ce-126">Specifies the name of the resource group.</span></span>

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

### <span data-ttu-id="987ce-127">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="987ce-127">-TargetResourceId</span></span>
<span data-ttu-id="987ce-128">Hedef kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="987ce-128">Specifies the ID of the target resource.</span></span>

```yaml
Type: System.String
Parameter Sets: Parameters for Get-AzureRmAlertRule cmdlet using target resource uri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="987ce-129">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="987ce-129">-DefaultProfile</span></span>
<span data-ttu-id="987ce-130">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="987ce-130">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="987ce-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="987ce-131">CommonParameters</span></span>
<span data-ttu-id="987ce-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="987ce-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="987ce-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="987ce-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="987ce-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="987ce-134">INPUTS</span></span>

## <span data-ttu-id="987ce-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="987ce-135">OUTPUTS</span></span>

### <span data-ttu-id="987ce-136">System. Koleksiyonlar. Generic. LIST ' 1 [Microsoft. Azure. Commands. Insights. OutputClasses. Psmanagementıtemdescriptor]</span><span class="sxs-lookup"><span data-stu-id="987ce-136">System.Collections.Generic.List\`1[Microsoft.Azure.Commands.Insights.OutputClasses.PSManagementItemDescriptor]</span></span>

## <span data-ttu-id="987ce-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="987ce-137">NOTES</span></span>

## <span data-ttu-id="987ce-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="987ce-138">RELATED LINKS</span></span>

[<span data-ttu-id="987ce-139">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="987ce-139">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="987ce-140">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="987ce-140">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="987ce-141">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="987ce-141">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="987ce-142">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="987ce-142">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="987ce-143">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="987ce-143">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



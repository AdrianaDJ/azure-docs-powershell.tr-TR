---
external help file: Microsoft.Azure.Commands.Insights.dll-Help.xml
Module Name: AzureRM.Insights
ms.assetid: A837077C-0A79-431C-93D2-799B2134EE69
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.insights/get-azurermalertrule
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Insights/Commands.Insights/help/Get-AzureRmAlertRule.md
ms.openlocfilehash: 04112d84acb8b18ef4251aae86b9bdd00924993a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586694"
---
# <span data-ttu-id="595f5-101">Get-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="595f5-101">Get-AzureRmAlertRule</span></span>

## <span data-ttu-id="595f5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="595f5-102">SYNOPSIS</span></span>
<span data-ttu-id="595f5-103">Uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="595f5-103">Gets alert rules.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="595f5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="595f5-104">SYNTAX</span></span>

### <span data-ttu-id="595f5-105">GetByResourceGroup</span><span class="sxs-lookup"><span data-stu-id="595f5-105">GetByResourceGroup</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595f5-106">GetByName</span><span class="sxs-lookup"><span data-stu-id="595f5-106">GetByName</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -Name <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="595f5-107">GetByResourceUri</span><span class="sxs-lookup"><span data-stu-id="595f5-107">GetByResourceUri</span></span>
```
Get-AzureRmAlertRule -ResourceGroupName <String> -TargetResourceId <String> [-DetailedOutput] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="595f5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="595f5-108">DESCRIPTION</span></span>
<span data-ttu-id="595f5-109">**Get-AzureRmAlertRule** cmdlet 'i, adı veya URI 'sini ya da belirtilen bir kaynak grubundaki tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="595f5-109">The **Get-AzureRmAlertRule** cmdlet gets an alert rule by its name or URI, or all alert rules from a specified resource group.</span></span>

## <span data-ttu-id="595f5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="595f5-110">EXAMPLES</span></span>

### <span data-ttu-id="595f5-111">Örnek 1: kaynak grubu için uyarı kurallarını alma</span><span class="sxs-lookup"><span data-stu-id="595f5-111">Example 1: Get alert rules for a resource group</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS"
```

<span data-ttu-id="595f5-112">Bu komut, Default-Web-merkezileştirme adlı kaynak grubu için tüm uyarı kurallarını alır.</span><span class="sxs-lookup"><span data-stu-id="595f5-112">This command gets all of the alert rules for the resource group named Default-Web-CentralUS.</span></span>
<span data-ttu-id="595f5-113">*DetailedOutput* parametresi belirtilmediğinden, çıktı kurallarla ilgili ayrıntıları içermez.</span><span class="sxs-lookup"><span data-stu-id="595f5-113">The output does not contain details about the rules because the *DetailedOutput* parameter is not specified.</span></span>

### <span data-ttu-id="595f5-114">Örnek 2: ada göre bir uyarı kuralı alma</span><span class="sxs-lookup"><span data-stu-id="595f5-114">Example 2: Get an alert rule by name</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourcGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8"
```

<span data-ttu-id="595f5-115">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="595f5-115">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="595f5-116">*DetailedOutput* parametresi belirtilmediğinden, çıkış yalnızca uyarı kuralıyla ilgili temel bilgileri içerir.</span><span class="sxs-lookup"><span data-stu-id="595f5-116">Because the *DetailedOutput* parameter is not specified, the output contains only basic information about the alert rule.</span></span>

### <span data-ttu-id="595f5-117">Örnek 3: ayrıntılı çıktıya sahip bir uyarı kuralı adı alın</span><span class="sxs-lookup"><span data-stu-id="595f5-117">Example 3: Get an alert rule by name with detailed output</span></span>
```
PS C:\>Get-AzureRmAlertRule -ResourceGroup "Default-Web-CentralUS" -Name "myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8" -DetailedOutput
```

<span data-ttu-id="595f5-118">Bu komut, myalert-7daıen 48-214r-42CA-b12b-b245bb8f0ac8 adlı uyarı kuralını alır.</span><span class="sxs-lookup"><span data-stu-id="595f5-118">This command gets the alert rule named myalert-7da64548-214d-42ca-b12b-b245bb8f0ac8.</span></span>
<span data-ttu-id="595f5-119">*DetailedOutput* parametresi belirtilmiştir, böylece çıktı ayrıntılıdır.</span><span class="sxs-lookup"><span data-stu-id="595f5-119">The *DetailedOutput* parameter is specified, so the output is detailed.</span></span>

## <span data-ttu-id="595f5-120">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="595f5-120">PARAMETERS</span></span>

### <span data-ttu-id="595f5-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="595f5-121">-DefaultProfile</span></span>
<span data-ttu-id="595f5-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="595f5-122">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="595f5-123">-DetailedOutput</span><span class="sxs-lookup"><span data-stu-id="595f5-123">-DetailedOutput</span></span>
<span data-ttu-id="595f5-124">Çıktıda tüm ayrıntıları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="595f5-124">Displays full details in the output.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f5-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="595f5-125">-Name</span></span>
<span data-ttu-id="595f5-126">Alınacak uyarı kuralının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="595f5-126">Specifies the name of the alert rule to get.</span></span>

```yaml
Type: String
Parameter Sets: GetByName
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f5-127">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="595f5-127">-ResourceGroupName</span></span>
<span data-ttu-id="595f5-128">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="595f5-128">Specifies the name of the resource group.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: ResourceGroup

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f5-129">-Targetresourceıd</span><span class="sxs-lookup"><span data-stu-id="595f5-129">-TargetResourceId</span></span>
<span data-ttu-id="595f5-130">Hedef kaynağın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="595f5-130">Specifies the ID of the target resource.</span></span>

```yaml
Type: String
Parameter Sets: GetByResourceUri
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="595f5-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="595f5-131">CommonParameters</span></span>
<span data-ttu-id="595f5-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="595f5-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="595f5-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="595f5-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="595f5-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="595f5-134">INPUTS</span></span>

### <span data-ttu-id="595f5-135">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="595f5-135">None</span></span>
<span data-ttu-id="595f5-136">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="595f5-136">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="595f5-137">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="595f5-137">OUTPUTS</span></span>

### <span data-ttu-id="595f5-138">Liste<Microsoft. Azure. Commands. Insights. OutputClasses. PSAlertRule></span><span class="sxs-lookup"><span data-stu-id="595f5-138">List<Microsoft.Azure.Commands.Insights.OutputClasses.PSAlertRule></span></span>

## <span data-ttu-id="595f5-139">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="595f5-139">NOTES</span></span>

## <span data-ttu-id="595f5-140">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="595f5-140">RELATED LINKS</span></span>

[<span data-ttu-id="595f5-141">Add-AzureRmLogAlertRule</span><span class="sxs-lookup"><span data-stu-id="595f5-141">Add-AzureRmLogAlertRule</span></span>](./Add-AzureRmLogAlertRule.md)

[<span data-ttu-id="595f5-142">Add-AzureRmMetricAlertRule</span><span class="sxs-lookup"><span data-stu-id="595f5-142">Add-AzureRmMetricAlertRule</span></span>](./Add-AzureRmMetricAlertRule.md)

[<span data-ttu-id="595f5-143">Add-AzureRmWebtestAlertRule</span><span class="sxs-lookup"><span data-stu-id="595f5-143">Add-AzureRmWebtestAlertRule</span></span>](./Add-AzureRmWebtestAlertRule.md)

[<span data-ttu-id="595f5-144">Get-AzureRmAlertHistory</span><span class="sxs-lookup"><span data-stu-id="595f5-144">Get-AzureRmAlertHistory</span></span>](./Get-AzureRmAlertHistory.md)

[<span data-ttu-id="595f5-145">Remove-AzureRmAlertRule</span><span class="sxs-lookup"><span data-stu-id="595f5-145">Remove-AzureRmAlertRule</span></span>](./Remove-AzureRmAlertRule.md)



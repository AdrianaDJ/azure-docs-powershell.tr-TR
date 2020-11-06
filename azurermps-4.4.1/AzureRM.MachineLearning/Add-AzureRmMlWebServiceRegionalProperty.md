---
external help file: Microsoft.Azure.Commands.MachineLearning.dll-Help.xml
Module Name: AzureRM.MachineLearning
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/MachineLearning/Commands.MachineLearning/help/Add-AzureRmMlWebServiceRegionalProperty.md
ms.openlocfilehash: 24f12a0e95ab7c233a08ec1ad0f4dc330583dd3b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93595150"
---
# <span data-ttu-id="bff69-101">Add-AzureRmMlWebServiceRegionalProperty</span><span class="sxs-lookup"><span data-stu-id="bff69-101">Add-AzureRmMlWebServiceRegionalProperty</span></span>

## <span data-ttu-id="bff69-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff69-102">SYNOPSIS</span></span>
<span data-ttu-id="bff69-103">Bölgesel Web hizmeti özellikleri oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bff69-103">Creates regional web service properties.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bff69-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bff69-104">SYNTAX</span></span>

```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName <String> -Name <String> -Region <String> [-Force]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff69-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bff69-105">DESCRIPTION</span></span>
<span data-ttu-id="bff69-106">Var olan bir Web hizmeti için Azure makine Learning bölgesel özelliklerini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bff69-106">Creates Azure Machine Learning regional properties for an existing web service.</span></span>

## <span data-ttu-id="bff69-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bff69-107">EXAMPLES</span></span>

### <span data-ttu-id="bff69-108">--------------------------Örnek 1: Batı merkezi ABD için yeni bölgesel özellikler--------------------------</span><span class="sxs-lookup"><span data-stu-id="bff69-108">--------------------------  Example 1: Add new regional properties for West Central US  --------------------------</span></span>
<span data-ttu-id="bff69-109">@ {paragraf = PS C: \\ \> }</span><span class="sxs-lookup"><span data-stu-id="bff69-109">@{paragraph=PS C:\\\>}</span></span>



```
Add-AzureRmMlWebServiceRegionalProperty -ResourceGroupName "myresourcegroup" -Name "mywebservicename" -Region westcentralus
```

<span data-ttu-id="bff69-110">Bu örnek komut, "Batı merkezi" bölgesindeki bir Web hizmeti için bölgesel özellik oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bff69-110">This example command creates regional property for a  web service in the "West Central US" region.</span></span>

## <span data-ttu-id="bff69-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bff69-111">PARAMETERS</span></span>

### <span data-ttu-id="bff69-112">-Force</span><span class="sxs-lookup"><span data-stu-id="bff69-112">-Force</span></span>
<span data-ttu-id="bff69-113">Onay sorma.</span><span class="sxs-lookup"><span data-stu-id="bff69-113">Do not ask for confirmation.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff69-114">-Ad</span><span class="sxs-lookup"><span data-stu-id="bff69-114">-Name</span></span>
<span data-ttu-id="bff69-115">Web hizmetinin adı.</span><span class="sxs-lookup"><span data-stu-id="bff69-115">The name for the web service.</span></span>

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

### <span data-ttu-id="bff69-116">-Bölge</span><span class="sxs-lookup"><span data-stu-id="bff69-116">-Region</span></span>
<span data-ttu-id="bff69-117">Web hizmeti özelliklerinin oluşturulacağı bölge.</span><span class="sxs-lookup"><span data-stu-id="bff69-117">The region in which to create the web service properties.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff69-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff69-118">-ResourceGroupName</span></span>
<span data-ttu-id="bff69-119">Web servisinin ait olduğu kaynak grubu.</span><span class="sxs-lookup"><span data-stu-id="bff69-119">The resource group in which the web service belongs.</span></span>

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

### <span data-ttu-id="bff69-120">-Onay</span><span class="sxs-lookup"><span data-stu-id="bff69-120">-Confirm</span></span>
<span data-ttu-id="bff69-121">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bff69-121">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff69-122">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff69-122">-WhatIf</span></span>
<span data-ttu-id="bff69-123">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bff69-123">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff69-124">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bff69-124">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bff69-125">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff69-125">-DefaultProfile</span></span>
<span data-ttu-id="bff69-126">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bff69-126">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff69-127">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff69-127">CommonParameters</span></span>
<span data-ttu-id="bff69-128">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bff69-128">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff69-129">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bff69-129">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff69-130">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bff69-130">INPUTS</span></span>

## <span data-ttu-id="bff69-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bff69-131">OUTPUTS</span></span>

### <span data-ttu-id="bff69-132">Microsoft. Azure. Management. machinöğrenim. WebServices. modeller. Web</span><span class="sxs-lookup"><span data-stu-id="bff69-132">Microsoft.Azure.Management.MachineLearning.WebServices.Models.WebService</span></span>
<span data-ttu-id="bff69-133">Azure Machine Learning Web hizmetinin Özet açıklaması.</span><span class="sxs-lookup"><span data-stu-id="bff69-133">A summary description of the Azure Machine Learning web service.</span></span>

## <span data-ttu-id="bff69-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bff69-134">NOTES</span></span>
<span data-ttu-id="bff69-135">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, makine, makine Learning, azureml</span><span class="sxs-lookup"><span data-stu-id="bff69-135">Keywords: azure, azurerm, arm, resource, management, manager, machine, machine learning, azureml</span></span>

## <span data-ttu-id="bff69-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bff69-136">RELATED LINKS</span></span>


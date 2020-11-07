---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ApplicationInsights.dll-Help.xml
Module Name: Az.ApplicationInsights
online version: https://docs.microsoft.com/en-us/powershell/module/az.applicationinsights/get-azapplicationinsightsapikey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ApplicationInsights/ApplicationInsights/help/Get-AzApplicationInsightsApiKey.md
ms.openlocfilehash: bf5051f22d06e9e248501ecfb602bd47d3faaf39
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753384"
---
# <span data-ttu-id="c6c7c-101">Get-AzApplicationInsightsApiKey</span><span class="sxs-lookup"><span data-stu-id="c6c7c-101">Get-AzApplicationInsightsApiKey</span></span>

## <span data-ttu-id="c6c7c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6c7c-102">SYNOPSIS</span></span>
<span data-ttu-id="c6c7c-103">Application Insights kaynağı için Application Insights API 'si anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c6c7c-103">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c6c7c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6c7c-104">SYNTAX</span></span>

### <span data-ttu-id="c6c7c-105">ComponentNameParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c6c7c-105">ComponentNameParameterSet (Default)</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceGroupName] <String> [-Name] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c7c-106">Bileşen Entobjectparameterparameteri</span><span class="sxs-lookup"><span data-stu-id="c6c7c-106">ComponentObjectParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ApplicationInsightsComponent] <PSApplicationInsightsComponent>
 [[-ApiKeyId] <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="c6c7c-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c6c7c-107">ResourceIdParameterSet</span></span>
```
Get-AzApplicationInsightsApiKey [-ResourceId] <String> [[-ApiKeyId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="c6c7c-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6c7c-108">DESCRIPTION</span></span>
<span data-ttu-id="c6c7c-109">Application Insights kaynağı için Application Insights API 'si anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="c6c7c-109">Get application insights api keys for an application insights resource</span></span>

## <span data-ttu-id="c6c7c-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6c7c-110">EXAMPLES</span></span>

### <span data-ttu-id="c6c7c-111">Örnek 1 bir Application Insights kaynağı için API anahtarları alma</span><span class="sxs-lookup"><span data-stu-id="c6c7c-111">Example 1 Get Api Keys for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"

Id                                   Description Permissions                       CreatedDate                   ApiKey
--                                   ----------- -----------                       -----------                   ------
7c4c61dc-b392-4aa4-992f-ee92b84e5dee test1 ReadTelemetry                     Wed, 18 Oct 2017 23:36:40 GMT
63657030-dea6-4c52-82f4-6f5128cb92cb test2  {ReadTelemetry, WriteAnnotations} Wed, 18 Oct 2017 21:46:41 GMT
82549f39-f3ae-492e-8f94-f7aada75fa57 test3  ReadTelemetry                     Wed, 18 Oct 2017 22:30:23 GMT
```

<span data-ttu-id="c6c7c-112">"TestGroup" kaynak grubundaki "test" kaynağı için Application Insights API 'si anahtarlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-112">Get application insights api keys for resource "test" in resource group "testGroup".</span></span>

### <span data-ttu-id="c6c7c-113">Örnek 2 bir Application Insights kaynağı için belirli bir API anahtarı alma</span><span class="sxs-lookup"><span data-stu-id="c6c7c-113">Example 2 Get specific API key for an application insights resource</span></span>
```
PS C:\>  Get-AzApplicationInsightsApiKey -ResourceGroupName "testGroup" -Name "test"  -ApiKeyId 
7c4c61dc-b392-4aa4-992f-ee92b84e5dee
ApiKey      :
CreatedDate : Wed, 18 Oct 2017 23:36:40 GMT
Id          : 7c4c61dc-b392-4aa4-992f-ee92b84e5dee
Permissions : {ReadTelemetry}
Description : test1
```

<span data-ttu-id="c6c7c-114">"TestGroup" Resource grubundaki "dd173f38-4fd1-4C75-8af5-9 9c29aa0f867" kaynak</span><span class="sxs-lookup"><span data-stu-id="c6c7c-114">Get specific application insights api key that id is "dd173f38-4fd1-4c75-8af5-9 9c29aa0f867" for resource "test" in resource group "testGroup".</span></span>

## <span data-ttu-id="c6c7c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6c7c-115">PARAMETERS</span></span>

### <span data-ttu-id="c6c7c-116">-Apıkeyıd</span><span class="sxs-lookup"><span data-stu-id="c6c7c-116">-ApiKeyId</span></span>
<span data-ttu-id="c6c7c-117">Application Insights API anahtar kimliği.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-117">Application Insights Api Key Id.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c7c-118">-Applicationınsightscomponent</span><span class="sxs-lookup"><span data-stu-id="c6c7c-118">-ApplicationInsightsComponent</span></span>
<span data-ttu-id="c6c7c-119">Application Insights bileşen nesnesi.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-119">Application Insights Component Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent
Parameter Sets: ComponentObjectParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c7c-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6c7c-120">-DefaultProfile</span></span>
<span data-ttu-id="c6c7c-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c6c7c-122">-Ad</span><span class="sxs-lookup"><span data-stu-id="c6c7c-122">-Name</span></span>
<span data-ttu-id="c6c7c-123">Application Insights bileşen adı.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-123">Application Insights Component Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases: ApplicationInsightsComponentName, ComponentName

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c7c-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6c7c-124">-ResourceGroupName</span></span>
<span data-ttu-id="c6c7c-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-125">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ComponentNameParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c6c7c-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c6c7c-126">-ResourceId</span></span>
<span data-ttu-id="c6c7c-127">Application Insights bileşeni kaynak kimliği.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-127">Application Insights Component Resource Id.</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="c6c7c-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6c7c-128">CommonParameters</span></span>
<span data-ttu-id="c6c7c-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6c7c-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6c7c-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c6c7c-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6c7c-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6c7c-131">INPUTS</span></span>

### <span data-ttu-id="c6c7c-132">Microsoft. Azure. Commands. ApplicationInsights. modeller. PSApplicationInsightsComponent</span><span class="sxs-lookup"><span data-stu-id="c6c7c-132">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApplicationInsightsComponent</span></span>

### <span data-ttu-id="c6c7c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="c6c7c-133">System.String</span></span>

## <span data-ttu-id="c6c7c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6c7c-134">OUTPUTS</span></span>

### <span data-ttu-id="c6c7c-135">Microsoft. Azure. Commands. ApplicationInsights. model. PSApiKey</span><span class="sxs-lookup"><span data-stu-id="c6c7c-135">Microsoft.Azure.Commands.ApplicationInsights.Models.PSApiKey</span></span>

## <span data-ttu-id="c6c7c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6c7c-136">NOTES</span></span>

## <span data-ttu-id="c6c7c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6c7c-137">RELATED LINKS</span></span>

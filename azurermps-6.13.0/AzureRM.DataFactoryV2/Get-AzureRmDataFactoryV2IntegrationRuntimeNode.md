---
external help file: Microsoft.Azure.Commands.DataFactoryV2.dll-Help.xml
Module Name: AzureRM.DataFactoryV2
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datafactories/get-azurermdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataFactoryV2/Commands.DataFactoryV2/help/Get-AzureRmDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: e8f631b485c62dba2e3871d5c2deec69881097af
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762971"
---
# <span data-ttu-id="2dfe3-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="2dfe3-101">Get-AzureRmDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="2dfe3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="2dfe3-102">SYNOPSIS</span></span>
<span data-ttu-id="2dfe3-103">Tümleştirme çalışma zamanı düğümü bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-103">Gets an integration runtime node infomation.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="2dfe3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="2dfe3-104">SYNTAX</span></span>

### <span data-ttu-id="2dfe3-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="2dfe3-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="2dfe3-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="2dfe3-106">ByResourceId</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="2dfe3-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="2dfe3-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzureRmDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress]
 [-InputObject] <PSIntegrationRuntime> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="2dfe3-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="2dfe3-108">DESCRIPTION</span></span>
<span data-ttu-id="2dfe3-109">**Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet 'i Integration Runtime düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-109">The **Get-AzureRmDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="2dfe3-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="2dfe3-110">EXAMPLES</span></span>

### <span data-ttu-id="2dfe3-111">Örnek 1: Tümleştirme çalışma zamanı düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              :
```

<span data-ttu-id="2dfe3-112">Cmdlet, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="2dfe3-113">Örnek 2: Tümleştirme çalışma zamanı düğümünün adres bilgilerini IP adresiyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzureRmDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

ResourceGroupName      : rg-test-dfv2
DataFactoryName        : test-df-eu2
IntegrationRuntimeName : test-selfhost-ir
Name                   : Node_1
MachineName            : Test-02
HostServiceUri         : https://Test-02.redmond.corp.microsoft.com:8050/HostServiceRemote.svc/
Status                 : Online
Capabilities           : {[serviceBusConnected, True], [httpsPortEnabled, True], [credentialInSync, True], [connectedToResourceManager, True]...}
VersionStatus          : UpToDate
Version                : 3.2.6519.3
RegisterTime           : 12/1/2017 6:48:15 AM
LastConnectTime        : 12/1/2017 7:35:03 AM
ExpiryTime             : 
LastStartTime          : 12/1/2017 6:49:26 AM
LastStopTime           : 
LastUpdateResult       : None
LastStartUpdateTime    : 
LastEndUpdateTime      : 
IsActiveDispatcher     : True
ConcurrentJobsLimit    : 
MaxConcurrentJobs      : 48
IpAddress              : 167.220.1.167
```

<span data-ttu-id="2dfe3-114">Cmdlet, IP adresi de içinde olmak üzere, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' içinde ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="2dfe3-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="2dfe3-115">PARAMETERS</span></span>

### <span data-ttu-id="2dfe3-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="2dfe3-116">-DataFactoryName</span></span>
<span data-ttu-id="2dfe3-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-117">The data factory name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfe3-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="2dfe3-118">-DefaultProfile</span></span>
<span data-ttu-id="2dfe3-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="2dfe3-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="2dfe3-120">-InputObject</span></span>
<span data-ttu-id="2dfe3-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-121">The integration runtime object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime
Parameter Sets: ByIntegrationRuntimeObject
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfe3-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="2dfe3-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="2dfe3-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-123">The integration runtime name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfe3-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="2dfe3-124">-IpAddress</span></span>
<span data-ttu-id="2dfe3-125">Tümleştirme çalışma zamanı düğümünün IP adresi.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="2dfe3-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="2dfe3-126">-Name</span></span>
<span data-ttu-id="2dfe3-127">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="2dfe3-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="2dfe3-128">-ResourceGroupName</span></span>
<span data-ttu-id="2dfe3-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-129">The resource group name.</span></span>

```yaml
Type: System.String
Parameter Sets: ByIntegrationRuntimeName
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfe3-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="2dfe3-130">-ResourceId</span></span>
<span data-ttu-id="2dfe3-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-131">The Azure resource ID.</span></span>

```yaml
Type: System.String
Parameter Sets: ByResourceId
Aliases: Id

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="2dfe3-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="2dfe3-132">CommonParameters</span></span>
<span data-ttu-id="2dfe3-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="2dfe3-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="2dfe3-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="2dfe3-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="2dfe3-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="2dfe3-135">INPUTS</span></span>

### <span data-ttu-id="2dfe3-136">System. String</span><span class="sxs-lookup"><span data-stu-id="2dfe3-136">System.String</span></span>

### <span data-ttu-id="2dfe3-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="2dfe3-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>
<span data-ttu-id="2dfe3-138">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="2dfe3-138">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="2dfe3-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="2dfe3-139">OUTPUTS</span></span>

### <span data-ttu-id="2dfe3-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanagedıntegrationruntimenode</span><span class="sxs-lookup"><span data-stu-id="2dfe3-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="2dfe3-141">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="2dfe3-141">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="2dfe3-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="2dfe3-142">NOTES</span></span>
<span data-ttu-id="2dfe3-143">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="2dfe3-143">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="2dfe3-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="2dfe3-144">RELATED LINKS</span></span>

[<span data-ttu-id="2dfe3-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="2dfe3-145">Get-AzureRmDataFactoryV2IntegrationRuntime</span></span>]()

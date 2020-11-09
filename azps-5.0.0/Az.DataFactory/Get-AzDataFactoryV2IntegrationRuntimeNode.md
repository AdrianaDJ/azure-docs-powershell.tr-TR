---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4d99a495863f93acfb97b290488fd0db24d69444
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321017"
---
# <span data-ttu-id="e4b5d-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="e4b5d-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="e4b5d-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e4b5d-102">SYNOPSIS</span></span>
<span data-ttu-id="e4b5d-103">Tümleştirme çalışma zamanı düğümü bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-103">Gets an integration runtime node information.</span></span>

## <span data-ttu-id="e4b5d-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e4b5d-104">SYNTAX</span></span>

### <span data-ttu-id="e4b5d-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e4b5d-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="e4b5d-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="e4b5d-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="e4b5d-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="e4b5d-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="e4b5d-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e4b5d-108">DESCRIPTION</span></span>
<span data-ttu-id="e4b5d-109">**Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet 'i Integration Runtime düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="e4b5d-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e4b5d-110">EXAMPLES</span></span>

### <span data-ttu-id="e4b5d-111">Örnek 1: Tümleştirme çalışma zamanı düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1'

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

<span data-ttu-id="e4b5d-112">Cmdlet, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="e4b5d-113">Örnek 2: Tümleştirme çalışma zamanı düğümünün adres bilgilerini IP adresiyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
```
PS C:\> Get-AzDataFactoryV2IntegrationRuntimeNode -ResourceGroupName 'rg-test-dfv2' -DataFactoryName 'test-df-eu2'  -IntegrationRuntimeName 'test-selfhost-ir' -Name 'Node_1' -IpAddress

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

<span data-ttu-id="e4b5d-114">Cmdlet, IP adresi de içinde olmak üzere, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' içinde ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="e4b5d-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e4b5d-115">PARAMETERS</span></span>

### <span data-ttu-id="e4b5d-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="e4b5d-116">-DataFactoryName</span></span>
<span data-ttu-id="e4b5d-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-117">The data factory name.</span></span>

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

### <span data-ttu-id="e4b5d-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e4b5d-118">-DefaultProfile</span></span>
<span data-ttu-id="e4b5d-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e4b5d-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="e4b5d-120">-InputObject</span></span>
<span data-ttu-id="e4b5d-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="e4b5d-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="e4b5d-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="e4b5d-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="e4b5d-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="e4b5d-124">-IpAddress</span></span>
<span data-ttu-id="e4b5d-125">Tümleştirme çalışma zamanı düğümünün IP adresi.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="e4b5d-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="e4b5d-126">-Name</span></span>
<span data-ttu-id="e4b5d-127">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="e4b5d-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e4b5d-128">-ResourceGroupName</span></span>
<span data-ttu-id="e4b5d-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-129">The resource group name.</span></span>

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

### <span data-ttu-id="e4b5d-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e4b5d-130">-ResourceId</span></span>
<span data-ttu-id="e4b5d-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="e4b5d-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e4b5d-132">CommonParameters</span></span>
<span data-ttu-id="e4b5d-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e4b5d-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e4b5d-134">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="e4b5d-134">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e4b5d-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e4b5d-135">INPUTS</span></span>

### <span data-ttu-id="e4b5d-136">System. String</span><span class="sxs-lookup"><span data-stu-id="e4b5d-136">System.String</span></span>

### <span data-ttu-id="e4b5d-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="e4b5d-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="e4b5d-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e4b5d-138">OUTPUTS</span></span>

### <span data-ttu-id="e4b5d-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanagedıntegrationruntimenode</span><span class="sxs-lookup"><span data-stu-id="e4b5d-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="e4b5d-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="e4b5d-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="e4b5d-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e4b5d-141">NOTES</span></span>
<span data-ttu-id="e4b5d-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="e4b5d-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="e4b5d-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e4b5d-143">RELATED LINKS</span></span>

[<span data-ttu-id="e4b5d-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="e4b5d-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataFactoryV2.dll-Help.xml
Module Name: Az.DataFactory
online version: https://docs.microsoft.com/en-us/powershell/module/az.datafactory/get-azdatafactoryv2integrationruntimenode
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataFactory/DataFactoryV2/help/Get-AzDataFactoryV2IntegrationRuntimeNode.md
ms.openlocfilehash: 4da5387d5506733ff5046fc34f43bcc003c2b8be
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917104"
---
# <span data-ttu-id="4a845-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="4a845-101">Get-AzDataFactoryV2IntegrationRuntimeNode</span></span>

## <span data-ttu-id="4a845-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="4a845-102">SYNOPSIS</span></span>
<span data-ttu-id="4a845-103">Tümleştirme çalışma zamanı düğümü bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-103">Gets an integration runtime node infomation.</span></span>

## <span data-ttu-id="4a845-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="4a845-104">SYNTAX</span></span>

### <span data-ttu-id="4a845-105">Byıntegrationruntimename (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="4a845-105">ByIntegrationRuntimeName (Default)</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-IntegrationRuntimeName] <String>
 [-ResourceGroupName] <String> [-DataFactoryName] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

### <span data-ttu-id="4a845-106">Byresourceıd</span><span class="sxs-lookup"><span data-stu-id="4a845-106">ByResourceId</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-ResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="4a845-107">Byıntegrationruntimeobject</span><span class="sxs-lookup"><span data-stu-id="4a845-107">ByIntegrationRuntimeObject</span></span>
```
Get-AzDataFactoryV2IntegrationRuntimeNode -Name <String> [-IpAddress] [-InputObject] <PSIntegrationRuntime>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="4a845-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="4a845-108">DESCRIPTION</span></span>
<span data-ttu-id="4a845-109">**Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet 'i Integration Runtime düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-109">The **Get-AzDataFactoryV2IntegrationRuntimeNode** cmdlet gets the detail information of an integration runtime node.</span></span>

## <span data-ttu-id="4a845-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="4a845-110">EXAMPLES</span></span>

### <span data-ttu-id="4a845-111">Örnek 1: Tümleştirme çalışma zamanı düğümünün ayrıntı bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-111">Example 1: Gets the detail information of an integration runtime node.</span></span>
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

<span data-ttu-id="4a845-112">Cmdlet, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-112">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2'.</span></span>

### <span data-ttu-id="4a845-113">Örnek 2: Tümleştirme çalışma zamanı düğümünün adres bilgilerini IP adresiyle birlikte alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-113">Example 2: Gets the detail information of an integration runtime node together with IP address.</span></span>
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

<span data-ttu-id="4a845-114">Cmdlet, IP adresi de içinde olmak üzere, ' test-df-EU2 ' Veri Fabrikası ' test-Selfhost-IR ' içinde ' Node_1 ' adlı düğümün bilgilerini alır.</span><span class="sxs-lookup"><span data-stu-id="4a845-114">The cmdlet gets information of node named 'Node_1' in self-hosted integration runtime 'test-selfhost-ir' in data factory 'test-df-eu2', including the IP address.</span></span>

## <span data-ttu-id="4a845-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="4a845-115">PARAMETERS</span></span>

### <span data-ttu-id="4a845-116">-DataFactoryName</span><span class="sxs-lookup"><span data-stu-id="4a845-116">-DataFactoryName</span></span>
<span data-ttu-id="4a845-117">Veri Fabrikası adı.</span><span class="sxs-lookup"><span data-stu-id="4a845-117">The data factory name.</span></span>

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

### <span data-ttu-id="4a845-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="4a845-118">-DefaultProfile</span></span>
<span data-ttu-id="4a845-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="4a845-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="4a845-120">-InputObject</span><span class="sxs-lookup"><span data-stu-id="4a845-120">-InputObject</span></span>
<span data-ttu-id="4a845-121">Integration Runtime nesnesi.</span><span class="sxs-lookup"><span data-stu-id="4a845-121">The integration runtime object.</span></span>

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

### <span data-ttu-id="4a845-122">-Integrationruntimename</span><span class="sxs-lookup"><span data-stu-id="4a845-122">-IntegrationRuntimeName</span></span>
<span data-ttu-id="4a845-123">Tümleştirme çalışma zamanı adı.</span><span class="sxs-lookup"><span data-stu-id="4a845-123">The integration runtime name.</span></span>

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

### <span data-ttu-id="4a845-124">-IPAddress</span><span class="sxs-lookup"><span data-stu-id="4a845-124">-IpAddress</span></span>
<span data-ttu-id="4a845-125">Tümleştirme çalışma zamanı düğümünün IP adresi.</span><span class="sxs-lookup"><span data-stu-id="4a845-125">The IP Address of integration runtime node.</span></span>

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

### <span data-ttu-id="4a845-126">-Ad</span><span class="sxs-lookup"><span data-stu-id="4a845-126">-Name</span></span>
<span data-ttu-id="4a845-127">Integration Runtime düğüm adı.</span><span class="sxs-lookup"><span data-stu-id="4a845-127">The integration runtime node name.</span></span>

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

### <span data-ttu-id="4a845-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="4a845-128">-ResourceGroupName</span></span>
<span data-ttu-id="4a845-129">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="4a845-129">The resource group name.</span></span>

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

### <span data-ttu-id="4a845-130">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="4a845-130">-ResourceId</span></span>
<span data-ttu-id="4a845-131">Azure Resource ID.</span><span class="sxs-lookup"><span data-stu-id="4a845-131">The Azure resource ID.</span></span>

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

### <span data-ttu-id="4a845-132">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="4a845-132">CommonParameters</span></span>
<span data-ttu-id="4a845-133">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="4a845-133">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="4a845-134">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="4a845-134">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="4a845-135">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="4a845-135">INPUTS</span></span>

### <span data-ttu-id="4a845-136">System. String</span><span class="sxs-lookup"><span data-stu-id="4a845-136">System.String</span></span>

### <span data-ttu-id="4a845-137">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psıntegrationruntime</span><span class="sxs-lookup"><span data-stu-id="4a845-137">Microsoft.Azure.Commands.DataFactoryV2.Models.PSIntegrationRuntime</span></span>

## <span data-ttu-id="4a845-138">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="4a845-138">OUTPUTS</span></span>

### <span data-ttu-id="4a845-139">Microsoft. Azure. Commands. DataFactoryV2. modeller. Psmanagedıntegrationruntimenode</span><span class="sxs-lookup"><span data-stu-id="4a845-139">Microsoft.Azure.Commands.DataFactoryV2.Models.PSManagedIntegrationRuntimeNode</span></span>

### <span data-ttu-id="4a845-140">Microsoft. Azure. Commands. DataFactoryV2. modeller. PSSelfHostedIntegrationRuntimeNode</span><span class="sxs-lookup"><span data-stu-id="4a845-140">Microsoft.Azure.Commands.DataFactoryV2.Models.PSSelfHostedIntegrationRuntimeNode</span></span>

## <span data-ttu-id="4a845-141">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="4a845-141">NOTES</span></span>
<span data-ttu-id="4a845-142">Anahtar sözcükler: Azure, azurerm, ARM, kaynak, yönetim, yönetici, veri, fabrika, kopyalama, Etkinlikler, tümleştirme çalışma zamanı</span><span class="sxs-lookup"><span data-stu-id="4a845-142">Keywords: azure, azurerm, arm, resource, management, manager, data, factories, copy, activities, integration runtime</span></span>

## <span data-ttu-id="4a845-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="4a845-143">RELATED LINKS</span></span>

[<span data-ttu-id="4a845-144">Get-AzDataFactoryV2IntegrationRuntime</span><span class="sxs-lookup"><span data-stu-id="4a845-144">Get-AzDataFactoryV2IntegrationRuntime</span></span>]()

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/get-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Get-AzContainerRegistryWebhook.md
ms.openlocfilehash: 231ff710e2c8c2945947ecf2d09845e635ee6244
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "93937569"
---
# <span data-ttu-id="7629f-101">Get-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="7629f-101">Get-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="7629f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7629f-102">SYNOPSIS</span></span>
<span data-ttu-id="7629f-103">Kapsayıcı kayıt defteri Web kancası alır.</span><span class="sxs-lookup"><span data-stu-id="7629f-103">Gets a container registry webhook.</span></span>

## <span data-ttu-id="7629f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7629f-104">SYNTAX</span></span>

### <span data-ttu-id="7629f-105">Listwebhobynameresourcegroupparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="7629f-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7629f-106">Showweb, Bynameresourcegroupparameterset</span><span class="sxs-lookup"><span data-stu-id="7629f-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7629f-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7629f-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7629f-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="7629f-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="7629f-109">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="7629f-109">ResourceIdParameterSet</span></span>
```
Get-AzContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="7629f-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="7629f-110">DESCRIPTION</span></span>
<span data-ttu-id="7629f-111">Get-AzContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defterinin belirli bir Web kancasını veya kapsayıcı kayıt defterinin tüm Web kancasını alır.</span><span class="sxs-lookup"><span data-stu-id="7629f-111">The Get-AzContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="7629f-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7629f-112">EXAMPLES</span></span>

### <span data-ttu-id="7629f-113">Örnek 1: kapsayıcı kayıt defterinin belirli bir Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="7629f-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="7629f-114">Kapsayıcı kayıt defterinin belirli bir Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="7629f-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="7629f-115">Örnek 2: kapsayıcı kayıt defterinin tüm Web kancaları</span><span class="sxs-lookup"><span data-stu-id="7629f-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="7629f-116">Kapsayıcı kayıt defterinin tüm Web kancaları 'nı alma</span><span class="sxs-lookup"><span data-stu-id="7629f-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="7629f-117">Örnek 3: yapılandırma ayrıntılarını içeren bir kapsayıcı kayıt defterinin belirtilen Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="7629f-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="7629f-118">Yapılandırma ayrıntılarını içeren bir kapsayıcı kayıt defterinin belirtilen Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="7629f-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="7629f-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7629f-119">PARAMETERS</span></span>

### <span data-ttu-id="7629f-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7629f-120">-DefaultProfile</span></span>
<span data-ttu-id="7629f-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7629f-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7629f-122">-Includeconfiguration</span><span class="sxs-lookup"><span data-stu-id="7629f-122">-IncludeConfiguration</span></span>
<span data-ttu-id="7629f-123">Web kancası için yapılandırma bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="7629f-123">Get the configuration information for a webhook.</span></span>

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

### <span data-ttu-id="7629f-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="7629f-124">-Name</span></span>
<span data-ttu-id="7629f-125">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="7629f-125">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7629f-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="7629f-126">-Registry</span></span>
<span data-ttu-id="7629f-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="7629f-127">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="7629f-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="7629f-128">-RegistryName</span></span>
<span data-ttu-id="7629f-129">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="7629f-129">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7629f-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7629f-130">-ResourceGroupName</span></span>
<span data-ttu-id="7629f-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="7629f-131">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7629f-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="7629f-132">-ResourceId</span></span>
<span data-ttu-id="7629f-133">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="7629f-133">The container registry Webhook resource id</span></span>

```yaml
Type: System.String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7629f-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7629f-134">CommonParameters</span></span>
<span data-ttu-id="7629f-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7629f-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7629f-136">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="7629f-136">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7629f-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7629f-137">INPUTS</span></span>

### <span data-ttu-id="7629f-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="7629f-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>

### <span data-ttu-id="7629f-139">System. String</span><span class="sxs-lookup"><span data-stu-id="7629f-139">System.String</span></span>

## <span data-ttu-id="7629f-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7629f-140">OUTPUTS</span></span>

### <span data-ttu-id="7629f-141">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="7629f-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="7629f-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7629f-142">NOTES</span></span>

## <span data-ttu-id="7629f-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7629f-143">RELATED LINKS</span></span>

[<span data-ttu-id="7629f-144">Yeni-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="7629f-144">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7629f-145">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="7629f-145">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7629f-146">Remove-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="7629f-146">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="7629f-147">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="7629f-147">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)
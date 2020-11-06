---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/get-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Get-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 4f20f177b172ab9b5372de6b95d821202e991000
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588964"
---
# <span data-ttu-id="f9dfd-101">Get-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="f9dfd-101">Get-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="f9dfd-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f9dfd-102">SYNOPSIS</span></span>
<span data-ttu-id="f9dfd-103">Kapsayıcı kayıt defteri Web kancası alır.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-103">Gets a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f9dfd-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f9dfd-104">SYNTAX</span></span>

### <span data-ttu-id="f9dfd-105">Listwebhobynameresourcegroupparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f9dfd-105">ListWebhookByNameResourceGroupParameterSet (Default)</span></span>
```
Get-AzureRmContainerRegistryWebhook [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dfd-106">Showweb, Bynameresourcegroupparameterset</span><span class="sxs-lookup"><span data-stu-id="f9dfd-106">ShowWebhookByNameResourceGroupParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-IncludeConfiguration] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dfd-107">ShowWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dfd-107">ShowWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-Name] <String> -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dfd-108">ListWebhookByRegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f9dfd-108">ListWebhookByRegistryObjectParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook -Registry <PSContainerRegistry> [-IncludeConfiguration]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="f9dfd-109">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="f9dfd-109">ResourceIdParameterSet</span></span>
```
Get-AzureRmContainerRegistryWebhook [-IncludeConfiguration] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="f9dfd-110">Tanım</span><span class="sxs-lookup"><span data-stu-id="f9dfd-110">DESCRIPTION</span></span>
<span data-ttu-id="f9dfd-111">Get-AzureRmContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defterinin belirli bir Web kancasını veya kapsayıcı kayıt defterinin tüm Web kancasını alır.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-111">The Get-AzureRmContainerRegistryWebhook cmdlet gets a specified webhook of container registry or all the webhooks of a container registry.</span></span>

## <span data-ttu-id="f9dfd-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f9dfd-112">EXAMPLES</span></span>

### <span data-ttu-id="f9dfd-113">Örnek 1: kapsayıcı kayıt defterinin belirli bir Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="f9dfd-113">Example 1: Get a specified webhook of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded
```

<span data-ttu-id="f9dfd-114">Kapsayıcı kayıt defterinin belirli bir Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="f9dfd-114">Get a specified webhook of a container registry</span></span>

### <span data-ttu-id="f9dfd-115">Örnek 2: kapsayıcı kayıt defterinin tüm Web kancaları</span><span class="sxs-lookup"><span data-stu-id="f9dfd-115">Example 2: Get all the webhooks of a container registry</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook04       westus     enabled                    {push, delete}  Succeeded
webhook05       westus     disabled                   {push, delete}  Succeeded
wh003           westus     enabled                    delete          Succeeded
```

<span data-ttu-id="f9dfd-116">Kapsayıcı kayıt defterinin tüm Web kancaları 'nı alma</span><span class="sxs-lookup"><span data-stu-id="f9dfd-116">Get all the webhooks of a container registry</span></span>

### <span data-ttu-id="f9dfd-117">Örnek 3: yapılandırma ayrıntılarını içeren bir kapsayıcı kayıt defterinin belirtilen Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="f9dfd-117">Example 3: Get a specified webhook of a container registry with configuration details</span></span>
```powershell
PS C:\>Get-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -IncludeConfiguration

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled                    {push, delete}  Succeeded  http://www.test.com/
```

<span data-ttu-id="f9dfd-118">Yapılandırma ayrıntılarını içeren bir kapsayıcı kayıt defterinin belirtilen Web kancasını alma</span><span class="sxs-lookup"><span data-stu-id="f9dfd-118">Get a specified webhook of a container registry with configuration details</span></span>

## <span data-ttu-id="f9dfd-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f9dfd-119">PARAMETERS</span></span>

### <span data-ttu-id="f9dfd-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f9dfd-120">-DefaultProfile</span></span>
<span data-ttu-id="f9dfd-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-121">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f9dfd-122">-Includeconfiguration</span><span class="sxs-lookup"><span data-stu-id="f9dfd-122">-IncludeConfiguration</span></span>
<span data-ttu-id="f9dfd-123">Web kancası için yapılandırma bilgilerini alın.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-123">Get the configuration information for a webhook.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-124">-Ad</span><span class="sxs-lookup"><span data-stu-id="f9dfd-124">-Name</span></span>
<span data-ttu-id="f9dfd-125">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-125">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: ShowWebhookByNameResourceGroupParameterSet, ShowWebhookByRegistryObjectParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-126">-Registry</span><span class="sxs-lookup"><span data-stu-id="f9dfd-126">-Registry</span></span>
<span data-ttu-id="f9dfd-127">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-127">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: ShowWebhookByRegistryObjectParameterSet, ListWebhookByRegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-128">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="f9dfd-128">-RegistryName</span></span>
<span data-ttu-id="f9dfd-129">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-129">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-130">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f9dfd-130">-ResourceGroupName</span></span>
<span data-ttu-id="f9dfd-131">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-131">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: ListWebhookByNameResourceGroupParameterSet, ShowWebhookByNameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-132">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="f9dfd-132">-ResourceId</span></span>
<span data-ttu-id="f9dfd-133">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f9dfd-133">The container registry Webhook resource id</span></span>

```yaml
Type: String
Parameter Sets: ResourceIdParameterSet
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f9dfd-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f9dfd-134">CommonParameters</span></span>
<span data-ttu-id="f9dfd-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f9dfd-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f9dfd-136">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f9dfd-136">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f9dfd-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f9dfd-137">INPUTS</span></span>

### <span data-ttu-id="f9dfd-138">Microsoft. Azure. Commands. ContainerRegistry. PSContainerRegistry</span><span class="sxs-lookup"><span data-stu-id="f9dfd-138">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry</span></span>
<span data-ttu-id="f9dfd-139">System. String</span><span class="sxs-lookup"><span data-stu-id="f9dfd-139">System.String</span></span>

## <span data-ttu-id="f9dfd-140">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f9dfd-140">OUTPUTS</span></span>

### <span data-ttu-id="f9dfd-141">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="f9dfd-141">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="f9dfd-142">System. Koleksiyonlar. Generic. IList ' 1 [[Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb, Microsoft. Azure. Commands. ContainerRegistry, Version = 1.0.0.0, Culture = neutral, PublicKeyToken = null]]</span><span class="sxs-lookup"><span data-stu-id="f9dfd-142">System.Collections.Generic.IList\`1[[Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook, Microsoft.Azure.Commands.ContainerRegistry, Version=1.0.0.0, Culture=neutral, PublicKeyToken=null]]</span></span>

## <span data-ttu-id="f9dfd-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f9dfd-143">NOTES</span></span>

## <span data-ttu-id="f9dfd-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f9dfd-144">RELATED LINKS</span></span>

[<span data-ttu-id="f9dfd-145">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="f9dfd-145">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f9dfd-146">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="f9dfd-146">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f9dfd-147">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="f9dfd-147">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="f9dfd-148">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="f9dfd-148">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

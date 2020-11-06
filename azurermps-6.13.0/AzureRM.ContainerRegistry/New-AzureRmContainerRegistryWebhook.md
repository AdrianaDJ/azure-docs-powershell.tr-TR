---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 6cee5cc10fc9cbb1af014e2ad500b38111fc3564
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93572849"
---
# <span data-ttu-id="bdd93-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bdd93-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="bdd93-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bdd93-102">SYNOPSIS</span></span>
<span data-ttu-id="bdd93-103">Kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bdd93-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="bdd93-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bdd93-104">SYNTAX</span></span>

### <span data-ttu-id="bdd93-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bdd93-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bdd93-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bdd93-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bdd93-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bdd93-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bdd93-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bdd93-108">DESCRIPTION</span></span>
<span data-ttu-id="bdd93-109">New-AzureRmContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bdd93-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="bdd93-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bdd93-110">EXAMPLES</span></span>

### <span data-ttu-id="bdd93-111">Örnek 1: kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bdd93-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="bdd93-112">Kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bdd93-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="bdd93-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bdd93-113">PARAMETERS</span></span>

### <span data-ttu-id="bdd93-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="bdd93-114">-Action</span></span>
<span data-ttu-id="bdd93-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="bdd93-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bdd93-116">-DefaultProfile</span></span>
<span data-ttu-id="bdd93-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bdd93-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bdd93-118">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="bdd93-118">-Header</span></span>
<span data-ttu-id="bdd93-119">Web kancası bildirimlerine eklenecek özel üstbilgiler.</span><span class="sxs-lookup"><span data-stu-id="bdd93-119">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="bdd93-120">-Location</span></span>
<span data-ttu-id="bdd93-121">Web kancası konumu.</span><span class="sxs-lookup"><span data-stu-id="bdd93-121">Webhook Location.</span></span>
<span data-ttu-id="bdd93-122">Kayıt defterinin konumu.</span><span class="sxs-lookup"><span data-stu-id="bdd93-122">Default to the location of the registry.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bdd93-123">-Name</span></span>
<span data-ttu-id="bdd93-124">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="bdd93-124">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="bdd93-125">-Registry</span></span>
<span data-ttu-id="bdd93-126">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bdd93-126">Container Registry Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="bdd93-127">-RegistryName</span></span>
<span data-ttu-id="bdd93-128">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="bdd93-128">Container Registry Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bdd93-129">-ResourceGroupName</span></span>
<span data-ttu-id="bdd93-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bdd93-130">Resource Group Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bdd93-131">-ResourceId</span></span>
<span data-ttu-id="bdd93-132">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bdd93-132">The container registry resource id</span></span>

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

### <span data-ttu-id="bdd93-133">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="bdd93-133">-Scope</span></span>
<span data-ttu-id="bdd93-134">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="bdd93-134">Webhook scope.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="bdd93-135">-Status</span></span>
<span data-ttu-id="bdd93-136">Web kancası durumu, varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="bdd93-136">Webhook status, default value is enabled</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bdd93-137">-Tag</span></span>
<span data-ttu-id="bdd93-138">Web kancası etiketleri.</span><span class="sxs-lookup"><span data-stu-id="bdd93-138">Webhook tags.</span></span>

```yaml
Type: System.Collections.Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-139">-URI</span><span class="sxs-lookup"><span data-stu-id="bdd93-139">-Uri</span></span>
<span data-ttu-id="bdd93-140">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="bdd93-140">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="bdd93-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="bdd93-141">-Confirm</span></span>
<span data-ttu-id="bdd93-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bdd93-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bdd93-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bdd93-143">-WhatIf</span></span>
<span data-ttu-id="bdd93-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bdd93-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bdd93-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bdd93-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bdd93-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bdd93-146">CommonParameters</span></span>
<span data-ttu-id="bdd93-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bdd93-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bdd93-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bdd93-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bdd93-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bdd93-149">INPUTS</span></span>

### <span data-ttu-id="bdd93-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bdd93-150">System.String</span></span>

## <span data-ttu-id="bdd93-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bdd93-151">OUTPUTS</span></span>

### <span data-ttu-id="bdd93-152">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bdd93-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="bdd93-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bdd93-153">NOTES</span></span>

## <span data-ttu-id="bdd93-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bdd93-154">RELATED LINKS</span></span>

[<span data-ttu-id="bdd93-155">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bdd93-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="bdd93-156">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bdd93-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="bdd93-157">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bdd93-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="bdd93-158">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bdd93-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

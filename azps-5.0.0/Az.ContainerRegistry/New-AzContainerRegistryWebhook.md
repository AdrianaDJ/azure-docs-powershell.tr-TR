---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: 8ea10f2acbe69e31bf80e35f0a8ea1577ffac6f5
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319574"
---
# <span data-ttu-id="bff62-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="bff62-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="bff62-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bff62-102">SYNOPSIS</span></span>
<span data-ttu-id="bff62-103">Kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bff62-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="bff62-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bff62-104">SYNTAX</span></span>

### <span data-ttu-id="bff62-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="bff62-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="bff62-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="bff62-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="bff62-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="bff62-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="bff62-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="bff62-108">DESCRIPTION</span></span>
<span data-ttu-id="bff62-109">New-AzContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="bff62-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="bff62-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bff62-110">EXAMPLES</span></span>

### <span data-ttu-id="bff62-111">Örnek 1: kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bff62-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="bff62-112">Kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="bff62-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="bff62-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bff62-113">PARAMETERS</span></span>

### <span data-ttu-id="bff62-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="bff62-114">-Action</span></span>
<span data-ttu-id="bff62-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="bff62-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="bff62-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bff62-116">-DefaultProfile</span></span>
<span data-ttu-id="bff62-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bff62-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bff62-118">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="bff62-118">-Header</span></span>
<span data-ttu-id="bff62-119">Web kancası bildirimlerine eklenecek özel üstbilgiler.</span><span class="sxs-lookup"><span data-stu-id="bff62-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="bff62-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="bff62-120">-Location</span></span>
<span data-ttu-id="bff62-121">Web kancası konumu.</span><span class="sxs-lookup"><span data-stu-id="bff62-121">Webhook Location.</span></span>
<span data-ttu-id="bff62-122">Kayıt defterinin konumu.</span><span class="sxs-lookup"><span data-stu-id="bff62-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="bff62-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="bff62-123">-Name</span></span>
<span data-ttu-id="bff62-124">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="bff62-124">Webhook Name.</span></span>

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

### <span data-ttu-id="bff62-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="bff62-125">-Registry</span></span>
<span data-ttu-id="bff62-126">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="bff62-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="bff62-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="bff62-127">-RegistryName</span></span>
<span data-ttu-id="bff62-128">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="bff62-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="bff62-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bff62-129">-ResourceGroupName</span></span>
<span data-ttu-id="bff62-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="bff62-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="bff62-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="bff62-131">-ResourceId</span></span>
<span data-ttu-id="bff62-132">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="bff62-132">The container registry resource id</span></span>

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

### <span data-ttu-id="bff62-133">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="bff62-133">-Scope</span></span>
<span data-ttu-id="bff62-134">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="bff62-134">Webhook scope.</span></span>

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

### <span data-ttu-id="bff62-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="bff62-135">-Status</span></span>
<span data-ttu-id="bff62-136">Web kancası durumu, varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="bff62-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="bff62-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="bff62-137">-Tag</span></span>
<span data-ttu-id="bff62-138">Web kancası etiketleri.</span><span class="sxs-lookup"><span data-stu-id="bff62-138">Webhook tags.</span></span>

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

### <span data-ttu-id="bff62-139">-URI</span><span class="sxs-lookup"><span data-stu-id="bff62-139">-Uri</span></span>
<span data-ttu-id="bff62-140">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="bff62-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="bff62-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="bff62-141">-Confirm</span></span>
<span data-ttu-id="bff62-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="bff62-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="bff62-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="bff62-143">-WhatIf</span></span>
<span data-ttu-id="bff62-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="bff62-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="bff62-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="bff62-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="bff62-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bff62-146">CommonParameters</span></span>
<span data-ttu-id="bff62-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bff62-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bff62-148">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="bff62-148">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bff62-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bff62-149">INPUTS</span></span>

### <span data-ttu-id="bff62-150">System. String</span><span class="sxs-lookup"><span data-stu-id="bff62-150">System.String</span></span>

## <span data-ttu-id="bff62-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bff62-151">OUTPUTS</span></span>

### <span data-ttu-id="bff62-152">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bff62-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="bff62-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bff62-153">NOTES</span></span>

## <span data-ttu-id="bff62-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bff62-154">RELATED LINKS</span></span>

[<span data-ttu-id="bff62-155">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bff62-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bff62-156">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bff62-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bff62-157">Remove-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bff62-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="bff62-158">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="bff62-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)
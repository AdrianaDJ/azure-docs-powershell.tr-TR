---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/new-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/New-AzContainerRegistryWebhook.md
ms.openlocfilehash: b4429bfc6baec6af03223e34c8aa59f640d9f518
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752597"
---
# <span data-ttu-id="e8178-101">New-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="e8178-101">New-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="e8178-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="e8178-102">SYNOPSIS</span></span>
<span data-ttu-id="e8178-103">Kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8178-103">Creates a container registry webhook.</span></span>

## <span data-ttu-id="e8178-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="e8178-104">SYNTAX</span></span>

### <span data-ttu-id="e8178-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="e8178-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="e8178-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="e8178-106">RegistryObjectParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="e8178-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="e8178-107">ResourceIdParameterSet</span></span>
```
New-AzContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="e8178-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="e8178-108">DESCRIPTION</span></span>
<span data-ttu-id="e8178-109">New-AzContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="e8178-109">The New-AzContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="e8178-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="e8178-110">EXAMPLES</span></span>

### <span data-ttu-id="e8178-111">Örnek 1: kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8178-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="e8178-112">Kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="e8178-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="e8178-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="e8178-113">PARAMETERS</span></span>

### <span data-ttu-id="e8178-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="e8178-114">-Action</span></span>
<span data-ttu-id="e8178-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="e8178-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

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

### <span data-ttu-id="e8178-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="e8178-116">-DefaultProfile</span></span>
<span data-ttu-id="e8178-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="e8178-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="e8178-118">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="e8178-118">-Header</span></span>
<span data-ttu-id="e8178-119">Web kancası bildirimlerine eklenecek özel üstbilgiler.</span><span class="sxs-lookup"><span data-stu-id="e8178-119">Custom headers that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="e8178-120">-Konum</span><span class="sxs-lookup"><span data-stu-id="e8178-120">-Location</span></span>
<span data-ttu-id="e8178-121">Web kancası konumu.</span><span class="sxs-lookup"><span data-stu-id="e8178-121">Webhook Location.</span></span>
<span data-ttu-id="e8178-122">Kayıt defterinin konumu.</span><span class="sxs-lookup"><span data-stu-id="e8178-122">Default to the location of the registry.</span></span>

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

### <span data-ttu-id="e8178-123">-Ad</span><span class="sxs-lookup"><span data-stu-id="e8178-123">-Name</span></span>
<span data-ttu-id="e8178-124">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="e8178-124">Webhook Name.</span></span>

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

### <span data-ttu-id="e8178-125">-Registry</span><span class="sxs-lookup"><span data-stu-id="e8178-125">-Registry</span></span>
<span data-ttu-id="e8178-126">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="e8178-126">Container Registry Object.</span></span>

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

### <span data-ttu-id="e8178-127">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="e8178-127">-RegistryName</span></span>
<span data-ttu-id="e8178-128">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="e8178-128">Container Registry Name.</span></span>

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

### <span data-ttu-id="e8178-129">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="e8178-129">-ResourceGroupName</span></span>
<span data-ttu-id="e8178-130">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="e8178-130">Resource Group Name.</span></span>

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

### <span data-ttu-id="e8178-131">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="e8178-131">-ResourceId</span></span>
<span data-ttu-id="e8178-132">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="e8178-132">The container registry resource id</span></span>

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

### <span data-ttu-id="e8178-133">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="e8178-133">-Scope</span></span>
<span data-ttu-id="e8178-134">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="e8178-134">Webhook scope.</span></span>

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

### <span data-ttu-id="e8178-135">-Durum</span><span class="sxs-lookup"><span data-stu-id="e8178-135">-Status</span></span>
<span data-ttu-id="e8178-136">Web kancası durumu, varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="e8178-136">Webhook status, default value is enabled</span></span>

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

### <span data-ttu-id="e8178-137">Etiketli</span><span class="sxs-lookup"><span data-stu-id="e8178-137">-Tag</span></span>
<span data-ttu-id="e8178-138">Web kancası etiketleri.</span><span class="sxs-lookup"><span data-stu-id="e8178-138">Webhook tags.</span></span>

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

### <span data-ttu-id="e8178-139">-URI</span><span class="sxs-lookup"><span data-stu-id="e8178-139">-Uri</span></span>
<span data-ttu-id="e8178-140">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="e8178-140">The service URI for the webhook to post notifications.</span></span>

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

### <span data-ttu-id="e8178-141">-Onay</span><span class="sxs-lookup"><span data-stu-id="e8178-141">-Confirm</span></span>
<span data-ttu-id="e8178-142">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="e8178-142">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="e8178-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="e8178-143">-WhatIf</span></span>
<span data-ttu-id="e8178-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="e8178-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="e8178-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="e8178-145">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="e8178-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="e8178-146">CommonParameters</span></span>
<span data-ttu-id="e8178-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="e8178-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="e8178-148">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="e8178-148">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="e8178-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="e8178-149">INPUTS</span></span>

### <span data-ttu-id="e8178-150">System. String</span><span class="sxs-lookup"><span data-stu-id="e8178-150">System.String</span></span>

## <span data-ttu-id="e8178-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="e8178-151">OUTPUTS</span></span>

### <span data-ttu-id="e8178-152">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="e8178-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="e8178-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="e8178-153">NOTES</span></span>

## <span data-ttu-id="e8178-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="e8178-154">RELATED LINKS</span></span>

[<span data-ttu-id="e8178-155">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="e8178-155">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e8178-156">Update-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="e8178-156">Update-AzContainerRegistryWebhook</span></span>](Update-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e8178-157">Remove-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="e8178-157">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)

[<span data-ttu-id="e8178-158">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="e8178-158">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)
---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/update-azcontainerregistrywebhook
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Update-AzContainerRegistryWebhook.md
ms.openlocfilehash: 2343b58891109d829a37131dff084b2b51e7f8ad
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268360"
---
# <span data-ttu-id="79aa5-101">Update-AzContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="79aa5-101">Update-AzContainerRegistryWebhook</span></span>

## <span data-ttu-id="79aa5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="79aa5-102">SYNOPSIS</span></span>
<span data-ttu-id="79aa5-103">Kapsayıcı kayıt defteri Web kancasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="79aa5-103">Updates a container registry webhook.</span></span>

## <span data-ttu-id="79aa5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="79aa5-104">SYNTAX</span></span>

### <span data-ttu-id="79aa5-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="79aa5-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>]
 [-Status <String>] [-Scope <String>] -ResourceId <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79aa5-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="79aa5-106">NameResourceGroupParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="79aa5-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="79aa5-107">WebhookObjectParameterSet</span></span>
```
Update-AzContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="79aa5-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="79aa5-108">DESCRIPTION</span></span>
<span data-ttu-id="79aa5-109">Update-AzContainerRegistryWebhook cmdlet 'i bir kapsayıcı kayıt defteri Web kancasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="79aa5-109">The Update-AzContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="79aa5-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="79aa5-110">EXAMPLES</span></span>

### <span data-ttu-id="79aa5-111">Örnek 1: varolan bir kapsayıcı kayıt defteri Web kancasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="79aa5-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="79aa5-112">Var olan kapsayıcı Registry Web kancasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="79aa5-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="79aa5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="79aa5-113">PARAMETERS</span></span>

### <span data-ttu-id="79aa5-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="79aa5-114">-Action</span></span>
<span data-ttu-id="79aa5-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="79aa5-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79aa5-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="79aa5-116">-DefaultProfile</span></span>
<span data-ttu-id="79aa5-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="79aa5-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="79aa5-118">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="79aa5-118">-Header</span></span>
<span data-ttu-id="79aa5-119">\[Web kancası bildirimlerine eklenecek ' Key = Value ' biçiminde boşlukla ayrılmış özel üstbilgiler \] .</span><span class="sxs-lookup"><span data-stu-id="79aa5-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="79aa5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="79aa5-120">-Name</span></span>
<span data-ttu-id="79aa5-121">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="79aa5-121">Webhook Name.</span></span>

```yaml
Type: System.String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79aa5-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="79aa5-122">-RegistryName</span></span>
<span data-ttu-id="79aa5-123">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="79aa5-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="79aa5-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="79aa5-124">-ResourceGroupName</span></span>
<span data-ttu-id="79aa5-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="79aa5-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="79aa5-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="79aa5-126">-ResourceId</span></span>
<span data-ttu-id="79aa5-127">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="79aa5-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="79aa5-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="79aa5-128">-Scope</span></span>
<span data-ttu-id="79aa5-129">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="79aa5-129">Webhook scope.</span></span>

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

### <span data-ttu-id="79aa5-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="79aa5-130">-Status</span></span>
<span data-ttu-id="79aa5-131">Web kancası durumu</span><span class="sxs-lookup"><span data-stu-id="79aa5-131">Webhook status</span></span>

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

### <span data-ttu-id="79aa5-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="79aa5-132">-Tag</span></span>
<span data-ttu-id="79aa5-133">' Key \[ = değer ' biçiminde boşlukla ayrılmış Etiketler \] .</span><span class="sxs-lookup"><span data-stu-id="79aa5-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="79aa5-134">-URI</span><span class="sxs-lookup"><span data-stu-id="79aa5-134">-Uri</span></span>
<span data-ttu-id="79aa5-135">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="79aa5-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: System.Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="79aa5-136">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-136">-Webhook</span></span>
<span data-ttu-id="79aa5-137">Kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="79aa5-137">Container Registry Webhook Object.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="79aa5-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="79aa5-138">-Confirm</span></span>
<span data-ttu-id="79aa5-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="79aa5-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="79aa5-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="79aa5-140">-WhatIf</span></span>
<span data-ttu-id="79aa5-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="79aa5-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="79aa5-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="79aa5-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="79aa5-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="79aa5-143">CommonParameters</span></span>
<span data-ttu-id="79aa5-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="79aa5-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="79aa5-145">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="79aa5-145">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="79aa5-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="79aa5-146">INPUTS</span></span>

### <span data-ttu-id="79aa5-147">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

### <span data-ttu-id="79aa5-148">System. String</span><span class="sxs-lookup"><span data-stu-id="79aa5-148">System.String</span></span>

## <span data-ttu-id="79aa5-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="79aa5-149">OUTPUTS</span></span>

### <span data-ttu-id="79aa5-150">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="79aa5-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="79aa5-151">NOTES</span></span>

## <span data-ttu-id="79aa5-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="79aa5-152">RELATED LINKS</span></span>

[<span data-ttu-id="79aa5-153">Yeni-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-153">New-AzContainerRegistryWebhook</span></span>](New-AzContainerRegistryWebhook.md)

[<span data-ttu-id="79aa5-154">Get-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-154">Get-AzContainerRegistryWebhook</span></span>](Get-AzContainerRegistryWebhook.md)

[<span data-ttu-id="79aa5-155">Test-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-155">Test-AzContainerRegistryWebhook</span></span>](Test-AzContainerRegistryWebhook.md)

[<span data-ttu-id="79aa5-156">Remove-Azcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="79aa5-156">Remove-AzContainerRegistryWebhook</span></span>](Remove-AzContainerRegistryWebhook.md)
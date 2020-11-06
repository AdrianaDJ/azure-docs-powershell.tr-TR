---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/new-azurermcontainerregistry
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/New-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 0a23cfb79c341fb4fcee5b5688b0780ba178e978
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93591037"
---
# <span data-ttu-id="c86a1-101">New-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="c86a1-101">New-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="c86a1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c86a1-102">SYNOPSIS</span></span>
<span data-ttu-id="c86a1-103">Kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c86a1-103">Creates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="c86a1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c86a1-104">SYNTAX</span></span>

### <span data-ttu-id="c86a1-105">NameResourceGroupParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c86a1-105">NameResourceGroupParameterSet (Default)</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="c86a1-106">RegistryObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="c86a1-106">RegistryObjectParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]>
 -Registry <PSContainerRegistry> [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-Location <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c86a1-107">Resourceıdparameterset</span><span class="sxs-lookup"><span data-stu-id="c86a1-107">ResourceIdParameterSet</span></span>
```
New-AzureRmContainerRegistryWebhook [-Name] <String> [-Uri] <Uri> [-Action] <String[]> [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] [-Location <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c86a1-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c86a1-108">DESCRIPTION</span></span>
<span data-ttu-id="c86a1-109">New-AzureRmContainerRegistryWebhook cmdlet 'i kapsayıcı kayıt defteri Web kancası oluşturur.</span><span class="sxs-lookup"><span data-stu-id="c86a1-109">The New-AzureRmContainerRegistryWebhook cmdlet creates a container registry webhook.</span></span>

## <span data-ttu-id="c86a1-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c86a1-110">EXAMPLES</span></span>

### <span data-ttu-id="c86a1-111">Örnek 1: kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c86a1-111">Example 1: Create a container registry webhook.</span></span>
```
PS C:\> New-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key="val"} -Location "east us" -Status Enabled -Scope "foo:*"

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="c86a1-112">Kapsayıcı kayıt defteri Web kancası oluşturun.</span><span class="sxs-lookup"><span data-stu-id="c86a1-112">Create a container registry webhook.</span></span>

## <span data-ttu-id="c86a1-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c86a1-113">PARAMETERS</span></span>

### <span data-ttu-id="c86a1-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="c86a1-114">-Action</span></span>
<span data-ttu-id="c86a1-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="c86a1-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: True
Position: 4
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="c86a1-116">-Confirm</span></span>
<span data-ttu-id="c86a1-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c86a1-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c86a1-118">-DefaultProfile</span></span>
<span data-ttu-id="c86a1-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c86a1-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="c86a1-120">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="c86a1-120">-Header</span></span>
<span data-ttu-id="c86a1-121">Web kancası bildirimlerine eklenecek özel üstbilgiler.</span><span class="sxs-lookup"><span data-stu-id="c86a1-121">Custom headers that will be added to the webhook notifications.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: WebhookHeaders

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-122">-Konum</span><span class="sxs-lookup"><span data-stu-id="c86a1-122">-Location</span></span>
<span data-ttu-id="c86a1-123">Web kancası konumu.</span><span class="sxs-lookup"><span data-stu-id="c86a1-123">Webhook Location.</span></span>
<span data-ttu-id="c86a1-124">Kayıt defterinin konumu.</span><span class="sxs-lookup"><span data-stu-id="c86a1-124">Default to the location of the registry.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookLocation

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-125">-Ad</span><span class="sxs-lookup"><span data-stu-id="c86a1-125">-Name</span></span>
<span data-ttu-id="c86a1-126">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="c86a1-126">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-127">-Registry</span><span class="sxs-lookup"><span data-stu-id="c86a1-127">-Registry</span></span>
<span data-ttu-id="c86a1-128">Kapsayıcısı.</span><span class="sxs-lookup"><span data-stu-id="c86a1-128">Container Registry Object.</span></span>

```yaml
Type: PSContainerRegistry
Parameter Sets: RegistryObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-129">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="c86a1-129">-RegistryName</span></span>
<span data-ttu-id="c86a1-130">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="c86a1-130">Container Registry Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: ContainerRegistryName

Required: True
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-131">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c86a1-131">-ResourceGroupName</span></span>
<span data-ttu-id="c86a1-132">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="c86a1-132">Resource Group Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-133">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="c86a1-133">-ResourceId</span></span>
<span data-ttu-id="c86a1-134">Kapsayıcı kayıt defteri kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c86a1-134">The container registry resource id</span></span>

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

### <span data-ttu-id="c86a1-135">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="c86a1-135">-Scope</span></span>
<span data-ttu-id="c86a1-136">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="c86a1-136">Webhook scope.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookScope

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-137">-Durum</span><span class="sxs-lookup"><span data-stu-id="c86a1-137">-Status</span></span>
<span data-ttu-id="c86a1-138">Web kancası durumu, varsayılan değer etkindir</span><span class="sxs-lookup"><span data-stu-id="c86a1-138">Webhook status, default value is enabled</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: WebhookStatus
Accepted values: enabled, disabled

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-139">Etiketli</span><span class="sxs-lookup"><span data-stu-id="c86a1-139">-Tag</span></span>
<span data-ttu-id="c86a1-140">Web kancası etiketleri.</span><span class="sxs-lookup"><span data-stu-id="c86a1-140">Webhook tags.</span></span>

```yaml
Type: Hashtable
Parameter Sets: (All)
Aliases: Tags

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-141">-URI</span><span class="sxs-lookup"><span data-stu-id="c86a1-141">-Uri</span></span>
<span data-ttu-id="c86a1-142">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="c86a1-142">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-143">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c86a1-143">-WhatIf</span></span>
<span data-ttu-id="c86a1-144">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c86a1-144">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c86a1-145">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c86a1-145">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="c86a1-146">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c86a1-146">CommonParameters</span></span>
<span data-ttu-id="c86a1-147">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c86a1-147">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c86a1-148">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="c86a1-148">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c86a1-149">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c86a1-149">INPUTS</span></span>

### <span data-ttu-id="c86a1-150">System. String</span><span class="sxs-lookup"><span data-stu-id="c86a1-150">System.String</span></span>

## <span data-ttu-id="c86a1-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c86a1-151">OUTPUTS</span></span>

### <span data-ttu-id="c86a1-152">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="c86a1-152">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="c86a1-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c86a1-153">NOTES</span></span>

## <span data-ttu-id="c86a1-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c86a1-154">RELATED LINKS</span></span>

[<span data-ttu-id="c86a1-155">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="c86a1-155">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c86a1-156">Update-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="c86a1-156">Update-AzureRmContainerRegistryWebhook</span></span>](Update-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c86a1-157">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="c86a1-157">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="c86a1-158">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="c86a1-158">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

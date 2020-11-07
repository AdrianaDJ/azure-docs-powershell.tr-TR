---
external help file: Microsoft.Azure.Commands.ContainerRegistry.dll-Help.xml
Module Name: AzureRM.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.containerregistry/update-azurermcontainerregistrycredential
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/ContainerRegistry/Commands.ContainerRegistry/help/Update-AzureRmContainerRegistryWebhook.md
ms.openlocfilehash: 7515046ed6e9fd6ba5c64b8123f8113b28b53f9b
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762746"
---
# <span data-ttu-id="581c7-101">Update-AzureRmContainerRegistryWebhook</span><span class="sxs-lookup"><span data-stu-id="581c7-101">Update-AzureRmContainerRegistryWebhook</span></span>

## <span data-ttu-id="581c7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="581c7-102">SYNOPSIS</span></span>
<span data-ttu-id="581c7-103">Kapsayıcı kayıt defteri Web kancasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="581c7-103">Updates a container registry webhook.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="581c7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="581c7-104">SYNTAX</span></span>

### <span data-ttu-id="581c7-105">Resourceıdparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="581c7-105">ResourceIdParameterSet (Default)</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>]
 [-Tag <Hashtable>] [-Status <String>] [-Scope <String>] -ResourceId <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="581c7-106">NameResourceGroupParameterSet</span><span class="sxs-lookup"><span data-stu-id="581c7-106">NameResourceGroupParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Name] <String> [-ResourceGroupName] <String> [-RegistryName] <String>
 [-Uri <Uri>] [-Action <String[]>] [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>]
 [-Scope <String>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="581c7-107">WebhookObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="581c7-107">WebhookObjectParameterSet</span></span>
```
Update-AzureRmContainerRegistryWebhook [-Uri <Uri>] [-Action <String[]>] -Webhook <PSContainerRegistryWebhook>
 [-Header <Hashtable>] [-Tag <Hashtable>] [-Status <String>] [-Scope <String>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="581c7-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="581c7-108">DESCRIPTION</span></span>
<span data-ttu-id="581c7-109">Update-AzureRmContainerRegistryWebhook cmdlet 'i bir kapsayıcı kayıt defteri Web kancasını güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="581c7-109">The Update-AzureRmContainerRegistryWebhook cmdlet updates a container registry webhook.</span></span>

## <span data-ttu-id="581c7-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="581c7-110">EXAMPLES</span></span>

### <span data-ttu-id="581c7-111">Örnek 1: varolan bir kapsayıcı kayıt defteri Web kancasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="581c7-111">Example 1: Update an existing container registry webhook.</span></span>
```powershell
PS C:\>Update-AzureRmContainerRegistryWebhook -ResourceGroupName "MyResourceGroup" -RegistryName "MyRegistry" -Name "webhook001" -Uri http://www.bing.com -Action Delete,Push -Header @{SpecialHeader='headerVal'} -Tag @{Key='val'} -Status Enabled -Scope 'foo:*'

Name            Location   Status     Scope           Actions         Provisioni ServiceUri
                                                                      ngState
----            --------   ------     -----           -------         ---------- ----------
webhook001      westus     enabled    foo:*           {push, delete}  Succeeded
```

<span data-ttu-id="581c7-112">Var olan kapsayıcı Registry Web kancasını güncelleyin.</span><span class="sxs-lookup"><span data-stu-id="581c7-112">Update an existing container registry webhook.</span></span>

## <span data-ttu-id="581c7-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="581c7-113">PARAMETERS</span></span>

### <span data-ttu-id="581c7-114">-Eylem</span><span class="sxs-lookup"><span data-stu-id="581c7-114">-Action</span></span>
<span data-ttu-id="581c7-115">Web kancasını bildirimleri gönderme konusunda tetikleyen eylemlerin boşlukla ayrılmış listesi.</span><span class="sxs-lookup"><span data-stu-id="581c7-115">Space separated list of actions that trigger the webhook to post notifications.</span></span>

```yaml
Type: String[]
Parameter Sets: (All)
Aliases: WebhookActions
Accepted values: delete, push

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581c7-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="581c7-116">-DefaultProfile</span></span>
<span data-ttu-id="581c7-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="581c7-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="581c7-118">-Üst bilgi</span><span class="sxs-lookup"><span data-stu-id="581c7-118">-Header</span></span>
<span data-ttu-id="581c7-119">\[Web kancası bildirimlerine eklenecek ' Key = Value ' biçiminde boşlukla ayrılmış özel üstbilgiler \] .</span><span class="sxs-lookup"><span data-stu-id="581c7-119">Space separated custom headers in 'key\[=value\]' format that will be added to the webhook notifications.</span></span>

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

### <span data-ttu-id="581c7-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="581c7-120">-Name</span></span>
<span data-ttu-id="581c7-121">Web kancası adı.</span><span class="sxs-lookup"><span data-stu-id="581c7-121">Webhook Name.</span></span>

```yaml
Type: String
Parameter Sets: NameResourceGroupParameterSet
Aliases: WebhookName, ResourceName

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581c7-122">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="581c7-122">-RegistryName</span></span>
<span data-ttu-id="581c7-123">Kapsayıcı kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="581c7-123">Container Registry Name.</span></span>

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

### <span data-ttu-id="581c7-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="581c7-124">-ResourceGroupName</span></span>
<span data-ttu-id="581c7-125">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="581c7-125">Resource Group Name.</span></span>

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

### <span data-ttu-id="581c7-126">-RESOURCEID</span><span class="sxs-lookup"><span data-stu-id="581c7-126">-ResourceId</span></span>
<span data-ttu-id="581c7-127">Kapsayıcı kayıt defteri Web kancası kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="581c7-127">The container registry Webhook resource id</span></span>

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

### <span data-ttu-id="581c7-128">-Kapsam</span><span class="sxs-lookup"><span data-stu-id="581c7-128">-Scope</span></span>
<span data-ttu-id="581c7-129">Web kancası kapsamı.</span><span class="sxs-lookup"><span data-stu-id="581c7-129">Webhook scope.</span></span>

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

### <span data-ttu-id="581c7-130">-Durum</span><span class="sxs-lookup"><span data-stu-id="581c7-130">-Status</span></span>
<span data-ttu-id="581c7-131">Web kancası durumu</span><span class="sxs-lookup"><span data-stu-id="581c7-131">Webhook status</span></span>

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

### <span data-ttu-id="581c7-132">Etiketli</span><span class="sxs-lookup"><span data-stu-id="581c7-132">-Tag</span></span>
<span data-ttu-id="581c7-133">' Key \[ = değer ' biçiminde boşlukla ayrılmış Etiketler \] .</span><span class="sxs-lookup"><span data-stu-id="581c7-133">Space separated tags in 'key\[=value\]' format.</span></span>

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

### <span data-ttu-id="581c7-134">-URI</span><span class="sxs-lookup"><span data-stu-id="581c7-134">-Uri</span></span>
<span data-ttu-id="581c7-135">Web kancası 'nun bildirim göndermeleri için hizmet URI 'SI.</span><span class="sxs-lookup"><span data-stu-id="581c7-135">The service URI for the webhook to post notifications.</span></span>

```yaml
Type: Uri
Parameter Sets: (All)
Aliases: WebhookUri

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="581c7-136">-Web kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-136">-Webhook</span></span>
<span data-ttu-id="581c7-137">Kapsayıcısı</span><span class="sxs-lookup"><span data-stu-id="581c7-137">Container Registry Webhook Object.</span></span>

```yaml
Type: PSContainerRegistryWebhook
Parameter Sets: WebhookObjectParameterSet
Aliases: 

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="581c7-138">-Onay</span><span class="sxs-lookup"><span data-stu-id="581c7-138">-Confirm</span></span>
<span data-ttu-id="581c7-139">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="581c7-139">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="581c7-140">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="581c7-140">-WhatIf</span></span>
<span data-ttu-id="581c7-141">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="581c7-141">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="581c7-142">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="581c7-142">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="581c7-143">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="581c7-143">CommonParameters</span></span>
<span data-ttu-id="581c7-144">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="581c7-144">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="581c7-145">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="581c7-145">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="581c7-146">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="581c7-146">INPUTS</span></span>

### <span data-ttu-id="581c7-147">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-147">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>
<span data-ttu-id="581c7-148">System. String</span><span class="sxs-lookup"><span data-stu-id="581c7-148">System.String</span></span>

## <span data-ttu-id="581c7-149">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="581c7-149">OUTPUTS</span></span>

### <span data-ttu-id="581c7-150">Microsoft. Azure. Commands. ContainerRegistry. Pscontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-150">Microsoft.Azure.Commands.ContainerRegistry.PSContainerRegistryWebhook</span></span>

## <span data-ttu-id="581c7-151">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="581c7-151">NOTES</span></span>

## <span data-ttu-id="581c7-152">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="581c7-152">RELATED LINKS</span></span>

[<span data-ttu-id="581c7-153">Yeni-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-153">New-AzureRmContainerRegistryWebhook</span></span>](New-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="581c7-154">Get-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-154">Get-AzureRmContainerRegistryWebhook</span></span>](Get-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="581c7-155">Test-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-155">Test-AzureRmContainerRegistryWebhook</span></span>](Test-AzureRmContainerRegistryWebhook.md)

[<span data-ttu-id="581c7-156">Remove-Azurermcontainerregistryweb kancası</span><span class="sxs-lookup"><span data-stu-id="581c7-156">Remove-AzureRmContainerRegistryWebhook</span></span>](Remove-AzureRmContainerRegistryWebhook.md)

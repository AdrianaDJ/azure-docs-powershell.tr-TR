---
external help file: Microsoft.Azure.PowerShell.Cmdlets.ContainerRegistry.dll-Help.xml
Module Name: Az.ContainerRegistry
online version: https://docs.microsoft.com/en-us/powershell/module/az.containerregistry/import-azcontainerregistryimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/ContainerRegistry/ContainerRegistry/help/Import-AzContainerRegistryImage.md
ms.openlocfilehash: 5fee8fec8d7b87629bfa46932662f430534fc695
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319590"
---
# <span data-ttu-id="d9aa2-101">Import-AzContainerRegistryImage</span><span class="sxs-lookup"><span data-stu-id="d9aa2-101">Import-AzContainerRegistryImage</span></span>

## <span data-ttu-id="d9aa2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d9aa2-102">SYNOPSIS</span></span>
<span data-ttu-id="d9aa2-103">Genel/Azure kayıt defterinden bir Azure Kapsayıcı kayıt defterine resim aktarma.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-103">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d9aa2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d9aa2-104">SYNTAX</span></span>

### <span data-ttu-id="d9aa2-105">Importımaresourceıd (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d9aa2-105">ImportImageByResourceId (Default)</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

### <span data-ttu-id="d9aa2-106">Importımagebyresourceıdwithcredential</span><span class="sxs-lookup"><span data-stu-id="d9aa2-106">ImportImageByResourceIdWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryResourceId <String> [-Mode <String>] [-TargetTag <String[]>]
 [-UntaggedTargetRepository <String[]>] [-Username <String>] -Password <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9aa2-107">Importımagebyregistryuri</span><span class="sxs-lookup"><span data-stu-id="d9aa2-107">ImportImageByRegistryUri</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d9aa2-108">Importımagebyregistryuriwithcredential</span><span class="sxs-lookup"><span data-stu-id="d9aa2-108">ImportImageByRegistryUriWithCredential</span></span>
```
Import-AzContainerRegistryImage -ResourceGroupName <String> -RegistryName <String> -SourceImage <String>
 -SourceRegistryUri <String> [-Mode <String>] [-TargetTag <String[]>] [-UntaggedTargetRepository <String[]>]
 [-Username <String>] -Password <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d9aa2-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d9aa2-109">DESCRIPTION</span></span>
<span data-ttu-id="d9aa2-110">Genel/Azure kayıt defterinden bir Azure Kapsayıcı kayıt defterine resim aktarma.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-110">Import image from a public/azure registry to an azure container registry.</span></span>

## <span data-ttu-id="d9aa2-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d9aa2-111">EXAMPLES</span></span>

### <span data-ttu-id="d9aa2-112">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d9aa2-112">Example 1</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage library/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryUri docker.io -TargetTag busybox:latest
```

<span data-ttu-id="d9aa2-113">BUSYBOX 'ı ACR 'e aktar.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-113">Import busybox to ACR.</span></span> <span data-ttu-id="d9aa2-114">Notu</span><span class="sxs-lookup"><span data-stu-id="d9aa2-114">Note:</span></span> 
* <span data-ttu-id="d9aa2-115">"kitaplık/" kaynağının kaynak resimden önce eklenmesi gerekir.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-115">"library/" need to be add before source image.</span></span> <span data-ttu-id="d9aa2-116">"BusyBox: latest" => "kitaplık/BUSYBOX: latest"</span><span class="sxs-lookup"><span data-stu-id="d9aa2-116">"busybox:latest" => "library/busybox:latest"</span></span>
* <span data-ttu-id="d9aa2-117">Kaynak kayıt defteri genel kullanıma sunulursa gerekli kimlik bilgileri</span><span class="sxs-lookup"><span data-stu-id="d9aa2-117">Credential needed if source registry is not publicly available</span></span>

### <span data-ttu-id="d9aa2-118">Örnek 2</span><span class="sxs-lookup"><span data-stu-id="d9aa2-118">Example 2</span></span>
```powershell
PS C:\> Import-AzContainerRegistryImage -SourceImage $SourceRegistry.azurecr.io/busybox:latest -ResourceGroupName $resourceGroupName -RegistryName $RegistryName -SourceRegistryResourceId $SourceACRID -TargetTag busybox:latest
```

<span data-ttu-id="d9aa2-119">Kaynak ACR 'den hedef ACR 'ye BUSYBOX alın.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-119">Import busybox from source ACR to target ACR.</span></span> <span data-ttu-id="d9aa2-120">Notu</span><span class="sxs-lookup"><span data-stu-id="d9aa2-120">Note:</span></span> 
* <span data-ttu-id="d9aa2-121">Kaynak kayıt defteri için Yönetici kullanıcısı devre dışı bırakılmışsa kimlik bilgileri gerekir.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-121">Credential needed if admin user for source registry was disabled.</span></span>

## <span data-ttu-id="d9aa2-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d9aa2-122">PARAMETERS</span></span>

### <span data-ttu-id="d9aa2-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d9aa2-123">-DefaultProfile</span></span>
<span data-ttu-id="d9aa2-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d9aa2-125">-Mod</span><span class="sxs-lookup"><span data-stu-id="d9aa2-125">-Mode</span></span>
<span data-ttu-id="d9aa2-126">Zorunlu olduğunda, var olan hedef etiketlerin üzerine yazılır.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-126">When Force, any existing target tags will be overwritten.</span></span>
<span data-ttu-id="d9aa2-127">NoForce olduğunda, herhangi bir kopyalama başlamadan önce var olan hedef Etiketler işlemi başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-127">When NoForce, any existing target tags will fail the operation before any copying begins.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: Force, NoForce

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-128">-Parola</span><span class="sxs-lookup"><span data-stu-id="d9aa2-128">-Password</span></span>
<span data-ttu-id="d9aa2-129">Kaynak kayıt defteriyle kimlik doğrulaması için kullanılan parola.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-129">The password used to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-130">-RegistryName</span><span class="sxs-lookup"><span data-stu-id="d9aa2-130">-RegistryName</span></span>
<span data-ttu-id="d9aa2-131">Hedef kayıt defteri adı.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-131">Target registry name.</span></span>

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

### <span data-ttu-id="d9aa2-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d9aa2-132">-ResourceGroupName</span></span>
<span data-ttu-id="d9aa2-133">Kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-133">Resource group name.</span></span>

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

### <span data-ttu-id="d9aa2-134">-SourceImage</span><span class="sxs-lookup"><span data-stu-id="d9aa2-134">-SourceImage</span></span>
<span data-ttu-id="d9aa2-135">Kaynak yansımanın Depo adı.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-135">Repository name of the source image.</span></span>

<span data-ttu-id="d9aa2-136">Depoya göre bir resim belirtin (' Hello-World ').</span><span class="sxs-lookup"><span data-stu-id="d9aa2-136">Specify an image by repository ('hello-world').</span></span>
<span data-ttu-id="d9aa2-137">Bu, ' en son ' etiketini kullanacaktır.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-137">This will use the 'latest' tag.</span></span>

<span data-ttu-id="d9aa2-138">Etikete göre resim belirtme (' Hello-World: latest ').</span><span class="sxs-lookup"><span data-stu-id="d9aa2-138">Specify an image by tag ('hello-world:latest').</span></span>

<span data-ttu-id="d9aa2-139">SHA256 tabanlı bildirim Özeti (' ') ile bir resim belirtin hello-world@sha256:abc123 .</span><span class="sxs-lookup"><span data-stu-id="d9aa2-139">Specify an image by sha256-based manifest digest ('hello-world@sha256:abc123').</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-140">-SourceRegistryResourceId</span><span class="sxs-lookup"><span data-stu-id="d9aa2-140">-SourceRegistryResourceId</span></span>
<span data-ttu-id="d9aa2-141">Kaynak Azure kapsayıcısı kayıt defterinin kaynak tanımlayıcısı.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-141">The resource identifier of the source Azure Container Registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceId, ImportImageByResourceIdWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-142">-SourceRegistryUri</span><span class="sxs-lookup"><span data-stu-id="d9aa2-142">-SourceRegistryUri</span></span>
<span data-ttu-id="d9aa2-143">Kaynak kayıt defterinin adresi (örneğin, ' mcr.microsoft.com ').</span><span class="sxs-lookup"><span data-stu-id="d9aa2-143">The address of the source registry (e.g. 'mcr.microsoft.com').</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByRegistryUri, ImportImageByRegistryUriWithCredential
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-144">-TargetTag</span><span class="sxs-lookup"><span data-stu-id="d9aa2-144">-TargetTag</span></span>
<span data-ttu-id="d9aa2-145">Refpo: Tag biçimindeki dizelerin listesi \[ \] .</span><span class="sxs-lookup"><span data-stu-id="d9aa2-145">List of strings of the form repo\[:tag\].</span></span>
<span data-ttu-id="d9aa2-146">Etiket atlandığında, kaynak kullanılacak (veya kaynak etiket de atlanırsa ' en son ').</span><span class="sxs-lookup"><span data-stu-id="d9aa2-146">When tag is omitted the source will be used (or 'latest' if source tag is also omitted).</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-147">-Untaggevseçtargetrepository</span><span class="sxs-lookup"><span data-stu-id="d9aa2-147">-UntaggedTargetRepository</span></span>
<span data-ttu-id="d9aa2-148">Yalnızca bildirim kopyası yapmak için depo adları dizelerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-148">List of strings of repository names to do a manifest only copy.</span></span>
<span data-ttu-id="d9aa2-149">Etiket oluşturulmayacak.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-149">No tag will be created.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-150">-Kullanıcı adı</span><span class="sxs-lookup"><span data-stu-id="d9aa2-150">-Username</span></span>
<span data-ttu-id="d9aa2-151">Kaynak kayıt defteriyle kimlik doğrulaması yapılacak Kullanıcı adı.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-151">The username to authenticate with the source registry.</span></span>

```yaml
Type: System.String
Parameter Sets: ImportImageByResourceIdWithCredential, ImportImageByRegistryUriWithCredential
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d9aa2-152">-Onay</span><span class="sxs-lookup"><span data-stu-id="d9aa2-152">-Confirm</span></span>
<span data-ttu-id="d9aa2-153">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-153">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d9aa2-154">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d9aa2-154">-WhatIf</span></span>
<span data-ttu-id="d9aa2-155">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-155">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d9aa2-156">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-156">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d9aa2-157">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d9aa2-157">CommonParameters</span></span>
<span data-ttu-id="d9aa2-158">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-158">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d9aa2-159">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d9aa2-159">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d9aa2-160">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d9aa2-160">INPUTS</span></span>

### <span data-ttu-id="d9aa2-161">System. String</span><span class="sxs-lookup"><span data-stu-id="d9aa2-161">System.String</span></span>

## <span data-ttu-id="d9aa2-162">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d9aa2-162">OUTPUTS</span></span>

### <span data-ttu-id="d9aa2-163">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="d9aa2-163">System.Boolean</span></span>

## <span data-ttu-id="d9aa2-164">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d9aa2-164">NOTES</span></span>

## <span data-ttu-id="d9aa2-165">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d9aa2-165">RELATED LINKS</span></span>

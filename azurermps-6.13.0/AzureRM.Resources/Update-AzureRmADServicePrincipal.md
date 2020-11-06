---
external help file: Microsoft.Azure.Commands.Resources.dll-Help.xml
Module Name: AzureRM.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.resources/update-azurermadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Resources/Commands.Resources/help/Update-AzureRmADServicePrincipal.md
ms.openlocfilehash: ce778da76b0dfc81a8438bdd0fdc3e0a20215843
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594837"
---
# <span data-ttu-id="f7848-101">Update-AzureRmADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7848-101">Update-AzureRmADServicePrincipal</span></span>

## <span data-ttu-id="f7848-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f7848-102">SYNOPSIS</span></span>
<span data-ttu-id="f7848-103">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f7848-103">Updates an existing azure active directory service principal.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="f7848-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f7848-104">SYNTAX</span></span>

### <span data-ttu-id="f7848-105">Spobjectivseçwithdisplaynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f7848-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzureRmADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7848-106">Spapplicationıdwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="f7848-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7848-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="f7848-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f7848-108">Inputobjectwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="f7848-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzureRmADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="f7848-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="f7848-109">DESCRIPTION</span></span>
<span data-ttu-id="f7848-110">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f7848-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="f7848-111">Bu hizmet sorumlusunun ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzureRmADSpCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7848-111">To update the credentials associated with this service principal, please use New-AzureRmADSpCredential cmdlet.</span></span> <span data-ttu-id="f7848-112">Temel uygulamayla ilişkili özellikleri güncelleştirmek için lütfen Update-AzureRmADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="f7848-112">To update the properties associated with the underlying application, please use Update-AzureRmADApplication cmdlet.</span></span>

## <span data-ttu-id="f7848-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f7848-113">EXAMPLES</span></span>

### <span data-ttu-id="f7848-114">Örnek 1-hizmet sorumlusunun görünen adını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="f7848-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="f7848-115">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunun görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="f7848-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="f7848-116">Örnek 2-boru kullanarak hizmet sorumlusunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="f7848-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzureRmADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzureRmADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="f7848-117">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunu ve hizmet sorumlusunun görünen adını "Yenisör" olarak güncelleştirmek için Update-AzureRmADServicePrincipal cmdlet 'ine sahip kanalları alır.</span><span class="sxs-lookup"><span data-stu-id="f7848-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzureRmADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="f7848-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f7848-118">PARAMETERS</span></span>

### <span data-ttu-id="f7848-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="f7848-119">-ApplicationId</span></span>
<span data-ttu-id="f7848-120">Güncelleştirilecek hizmet sorumlusunun uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="f7848-120">The application id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpApplicationIdWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f7848-121">-DefaultProfile</span></span>
<span data-ttu-id="f7848-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f7848-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f7848-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="f7848-123">-DisplayName</span></span>
<span data-ttu-id="f7848-124">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="f7848-124">The display name for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet, SPNWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-125">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="f7848-125">-Homepage</span></span>
<span data-ttu-id="f7848-126">Hizmet sorumlusu için ana sayfa.</span><span class="sxs-lookup"><span data-stu-id="f7848-126">The homepage for the service principal.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-127">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="f7848-127">-IdentifierUri</span></span>
<span data-ttu-id="f7848-128">Hizmet sorumlusunun tanımlayıcı URI 'leri.</span><span class="sxs-lookup"><span data-stu-id="f7848-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="f7848-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="f7848-129">-InputObject</span></span>
<span data-ttu-id="f7848-130">Güncelleştirilecek hizmet sorumlusunu temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="f7848-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="f7848-131">-KeyCredential</span></span>
<span data-ttu-id="f7848-132">Hizmet sorumlusu için anahtar kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f7848-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="f7848-133">-ObjectId</span></span>
<span data-ttu-id="f7848-134">Güncelleştirilecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="f7848-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.Guid
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="f7848-135">-PasswordCredential</span></span>
<span data-ttu-id="f7848-136">Hizmet sorumlusunun parola kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="f7848-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Version1_6.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="f7848-137">-ServicePrincipalName</span></span>
<span data-ttu-id="f7848-138">Güncelleştirilecek hizmet sorumlusunun SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="f7848-138">The SPN of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SPNWithDisplayNameParameterSet
Aliases: SPN

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f7848-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="f7848-139">-Confirm</span></span>
<span data-ttu-id="f7848-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f7848-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f7848-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f7848-141">-WhatIf</span></span>
<span data-ttu-id="f7848-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f7848-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f7848-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f7848-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f7848-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f7848-144">CommonParameters</span></span>
<span data-ttu-id="f7848-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f7848-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f7848-146">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f7848-146">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f7848-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f7848-147">INPUTS</span></span>

### <span data-ttu-id="f7848-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="f7848-148">System.Guid</span></span>

### <span data-ttu-id="f7848-149">System. String</span><span class="sxs-lookup"><span data-stu-id="f7848-149">System.String</span></span>

### <span data-ttu-id="f7848-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7848-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="f7848-151">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="f7848-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="f7848-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f7848-152">OUTPUTS</span></span>

### <span data-ttu-id="f7848-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="f7848-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="f7848-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f7848-154">NOTES</span></span>

## <span data-ttu-id="f7848-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f7848-155">RELATED LINKS</span></span>

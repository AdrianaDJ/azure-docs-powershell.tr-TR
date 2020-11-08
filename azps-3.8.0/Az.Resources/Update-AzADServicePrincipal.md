---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 19d8c4e3a47f7b75073d0207d000b8f18a5c0f6f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097173"
---
# <span data-ttu-id="3b752-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3b752-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="3b752-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="3b752-102">SYNOPSIS</span></span>
<span data-ttu-id="3b752-103">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b752-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="3b752-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="3b752-104">SYNTAX</span></span>

### <span data-ttu-id="3b752-105">Spobjectivseçwithdisplaynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="3b752-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b752-106">Spapplicationıdwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="3b752-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b752-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="3b752-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="3b752-108">Inputobjectwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="3b752-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="3b752-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="3b752-109">DESCRIPTION</span></span>
<span data-ttu-id="3b752-110">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b752-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="3b752-111">Bu hizmet sorumlusunun ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzADSpCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b752-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="3b752-112">Temel uygulamayla ilişkili özellikleri güncelleştirmek için lütfen Update-AzADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="3b752-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="3b752-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="3b752-113">EXAMPLES</span></span>

### <span data-ttu-id="3b752-114">Örnek 1-hizmet sorumlusunun görünen adını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="3b752-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="3b752-115">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunun görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="3b752-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="3b752-116">Örnek 2-boru kullanarak hizmet sorumlusunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="3b752-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="3b752-117">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunu ve hizmet sorumlusunun görünen adını "Yenisör" olarak güncelleştirmek için Update-AzADServicePrincipal cmdlet 'ine sahip kanalları alır.</span><span class="sxs-lookup"><span data-stu-id="3b752-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="3b752-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="3b752-118">PARAMETERS</span></span>

### <span data-ttu-id="3b752-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="3b752-119">-ApplicationId</span></span>
<span data-ttu-id="3b752-120">Güncelleştirilecek hizmet sorumlusunun uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="3b752-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="3b752-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="3b752-121">-DefaultProfile</span></span>
<span data-ttu-id="3b752-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="3b752-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="3b752-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="3b752-123">-DisplayName</span></span>
<span data-ttu-id="3b752-124">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="3b752-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="3b752-125">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="3b752-125">-Homepage</span></span>
<span data-ttu-id="3b752-126">Hizmet sorumlusu için ana sayfa.</span><span class="sxs-lookup"><span data-stu-id="3b752-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="3b752-127">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="3b752-127">-IdentifierUri</span></span>
<span data-ttu-id="3b752-128">Hizmet sorumlusunun tanımlayıcı URI 'leri.</span><span class="sxs-lookup"><span data-stu-id="3b752-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="3b752-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="3b752-129">-InputObject</span></span>
<span data-ttu-id="3b752-130">Güncelleştirilecek hizmet sorumlusunu temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="3b752-130">The object representing the service principal to update.</span></span>

```yaml
Type: Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal
Parameter Sets: InputObjectWithDisplayNameParameterSet
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="3b752-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="3b752-131">-KeyCredential</span></span>
<span data-ttu-id="3b752-132">Hizmet sorumlusu için anahtar kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b752-132">The key credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.KeyCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b752-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="3b752-133">-ObjectId</span></span>
<span data-ttu-id="3b752-134">Güncelleştirilecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="3b752-134">The object id of the service principal to update.</span></span>

```yaml
Type: System.String
Parameter Sets: SpObjectIdWithDisplayNameParameterSet
Aliases: ServicePrincipalObjectId

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="3b752-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="3b752-135">-PasswordCredential</span></span>
<span data-ttu-id="3b752-136">Hizmet sorumlusunun parola kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="3b752-136">The password credential(s) for the service principal.</span></span>

```yaml
Type: Microsoft.Azure.Graph.RBAC.Models.PasswordCredential[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="3b752-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="3b752-137">-ServicePrincipalName</span></span>
<span data-ttu-id="3b752-138">Güncelleştirilecek hizmet sorumlusunun SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="3b752-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="3b752-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="3b752-139">-Confirm</span></span>
<span data-ttu-id="3b752-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="3b752-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="3b752-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="3b752-141">-WhatIf</span></span>
<span data-ttu-id="3b752-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="3b752-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="3b752-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="3b752-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="3b752-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="3b752-144">CommonParameters</span></span>
<span data-ttu-id="3b752-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="3b752-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="3b752-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="3b752-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="3b752-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="3b752-147">INPUTS</span></span>

### <span data-ttu-id="3b752-148">System. String</span><span class="sxs-lookup"><span data-stu-id="3b752-148">System.String</span></span>

### <span data-ttu-id="3b752-149">System. Guid</span><span class="sxs-lookup"><span data-stu-id="3b752-149">System.Guid</span></span>

### <span data-ttu-id="3b752-150">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3b752-150">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3b752-151">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="3b752-151">OUTPUTS</span></span>

### <span data-ttu-id="3b752-152">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="3b752-152">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="3b752-153">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="3b752-153">NOTES</span></span>

## <span data-ttu-id="3b752-154">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="3b752-154">RELATED LINKS</span></span>

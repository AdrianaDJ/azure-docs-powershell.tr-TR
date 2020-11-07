---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-Azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: e2c8e8fea9f8f86f06a9808158c50cb63915106b
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93936295"
---
# <span data-ttu-id="d24f9-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d24f9-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="d24f9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d24f9-102">SYNOPSIS</span></span>
<span data-ttu-id="d24f9-103">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d24f9-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="d24f9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d24f9-104">SYNTAX</span></span>

### <span data-ttu-id="d24f9-105">Spobjectivseçwithdisplaynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="d24f9-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <Guid> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24f9-106">Spapplicationıdwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="d24f9-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24f9-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="d24f9-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="d24f9-108">Inputobjectwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="d24f9-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>]
 [-Homepage <String>] [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>]
 [-PasswordCredential <PasswordCredential[]>] [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="d24f9-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="d24f9-109">DESCRIPTION</span></span>
<span data-ttu-id="d24f9-110">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d24f9-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="d24f9-111">Bu hizmet sorumlusunun ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzADSpCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d24f9-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="d24f9-112">Temel uygulamayla ilişkili özellikleri güncelleştirmek için lütfen Update-AzADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="d24f9-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="d24f9-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d24f9-113">EXAMPLES</span></span>

### <span data-ttu-id="d24f9-114">Örnek 1-hizmet sorumlusunun görünen adını güncelleyin</span><span class="sxs-lookup"><span data-stu-id="d24f9-114">Example 1 - Update the display name of a service principal</span></span>

```
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="d24f9-115">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunun görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="d24f9-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="d24f9-116">Örnek 2-boru kullanarak hizmet sorumlusunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="d24f9-116">Example 2 - Update the display name of a service principal using piping</span></span>

```
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="d24f9-117">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunu ve hizmet sorumlusunun görünen adını "Yenisör" olarak güncelleştirmek için Update-AzADServicePrincipal cmdlet 'ine sahip kanalları alır.</span><span class="sxs-lookup"><span data-stu-id="d24f9-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

## <span data-ttu-id="d24f9-118">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d24f9-118">PARAMETERS</span></span>

### <span data-ttu-id="d24f9-119">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="d24f9-119">-ApplicationId</span></span>
<span data-ttu-id="d24f9-120">Güncelleştirilecek hizmet sorumlusunun uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="d24f9-120">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="d24f9-121">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d24f9-121">-DefaultProfile</span></span>
<span data-ttu-id="d24f9-122">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d24f9-122">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d24f9-123">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="d24f9-123">-DisplayName</span></span>
<span data-ttu-id="d24f9-124">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="d24f9-124">The display name for the service principal.</span></span>

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

### <span data-ttu-id="d24f9-125">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="d24f9-125">-Homepage</span></span>
<span data-ttu-id="d24f9-126">Hizmet sorumlusu için ana sayfa.</span><span class="sxs-lookup"><span data-stu-id="d24f9-126">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="d24f9-127">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="d24f9-127">-IdentifierUri</span></span>
<span data-ttu-id="d24f9-128">Hizmet sorumlusunun tanımlayıcı URI 'leri.</span><span class="sxs-lookup"><span data-stu-id="d24f9-128">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="d24f9-129">-InputObject</span><span class="sxs-lookup"><span data-stu-id="d24f9-129">-InputObject</span></span>
<span data-ttu-id="d24f9-130">Güncelleştirilecek hizmet sorumlusunu temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="d24f9-130">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="d24f9-131">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="d24f9-131">-KeyCredential</span></span>
<span data-ttu-id="d24f9-132">Hizmet sorumlusu için anahtar kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d24f9-132">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="d24f9-133">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="d24f9-133">-ObjectId</span></span>
<span data-ttu-id="d24f9-134">Güncelleştirilecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="d24f9-134">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="d24f9-135">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="d24f9-135">-PasswordCredential</span></span>
<span data-ttu-id="d24f9-136">Hizmet sorumlusunun parola kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="d24f9-136">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="d24f9-137">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="d24f9-137">-ServicePrincipalName</span></span>
<span data-ttu-id="d24f9-138">Güncelleştirilecek hizmet sorumlusunun SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="d24f9-138">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="d24f9-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="d24f9-139">-Confirm</span></span>
<span data-ttu-id="d24f9-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d24f9-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="d24f9-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d24f9-141">-WhatIf</span></span>
<span data-ttu-id="d24f9-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d24f9-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d24f9-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d24f9-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="d24f9-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d24f9-144">CommonParameters</span></span>
<span data-ttu-id="d24f9-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d24f9-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d24f9-146">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="d24f9-146">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d24f9-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d24f9-147">INPUTS</span></span>

### <span data-ttu-id="d24f9-148">System. Guid</span><span class="sxs-lookup"><span data-stu-id="d24f9-148">System.Guid</span></span>

### <span data-ttu-id="d24f9-149">System. String</span><span class="sxs-lookup"><span data-stu-id="d24f9-149">System.String</span></span>

### <span data-ttu-id="d24f9-150">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d24f9-150">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>
<span data-ttu-id="d24f9-151">Parametreler: InputObject (ByValue)</span><span class="sxs-lookup"><span data-stu-id="d24f9-151">Parameters: InputObject (ByValue)</span></span>

## <span data-ttu-id="d24f9-152">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d24f9-152">OUTPUTS</span></span>

### <span data-ttu-id="d24f9-153">Microsoft.Azure.Graph.RBAC.Version1_6. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="d24f9-153">Microsoft.Azure.Graph.RBAC.Version1_6.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="d24f9-154">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d24f9-154">NOTES</span></span>

## <span data-ttu-id="d24f9-155">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d24f9-155">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Resources.dll-Help.xml
Module Name: Az.Resources
online version: https://docs.microsoft.com/en-us/powershell/module/az.resources/update-azadserviceprincipal
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Resources/Resources/help/Update-AzADServicePrincipal.md
ms.openlocfilehash: 4a4888573199c4fd5f76282fb5c8eb1702911e00
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94107645"
---
# <span data-ttu-id="aa617-101">Update-AzADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aa617-101">Update-AzADServicePrincipal</span></span>

## <span data-ttu-id="aa617-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="aa617-102">SYNOPSIS</span></span>
<span data-ttu-id="aa617-103">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aa617-103">Updates an existing azure active directory service principal.</span></span>

## <span data-ttu-id="aa617-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="aa617-104">SYNTAX</span></span>

### <span data-ttu-id="aa617-105">Spobjectivseçwithdisplaynameparameterset (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="aa617-105">SpObjectIdWithDisplayNameParameterSet (Default)</span></span>
```
Update-AzADServicePrincipal -ObjectId <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa617-106">Spapplicationıdwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="aa617-106">SpApplicationIdWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ApplicationId <Guid> [-Homepage <String>] [-IdentifierUri <String[]>]
 [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa617-107">SPNWithDisplayNameParameterSet</span><span class="sxs-lookup"><span data-stu-id="aa617-107">SPNWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -ServicePrincipalName <String> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="aa617-108">Inputobjectwithdisplaynameparameterset</span><span class="sxs-lookup"><span data-stu-id="aa617-108">InputObjectWithDisplayNameParameterSet</span></span>
```
Update-AzADServicePrincipal -InputObject <PSADServicePrincipal> [-DisplayName <String>] [-Homepage <String>]
 [-IdentifierUri <String[]>] [-KeyCredential <KeyCredential[]>] [-PasswordCredential <PasswordCredential[]>]
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="aa617-109">Tanım</span><span class="sxs-lookup"><span data-stu-id="aa617-109">DESCRIPTION</span></span>
<span data-ttu-id="aa617-110">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aa617-110">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="aa617-111">Bu hizmet sorumlusunun ilişkili kimlik bilgilerini güncelleştirmek için lütfen New-AzADSpCredential cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aa617-111">To update the credentials associated with this service principal, please use New-AzADSpCredential cmdlet.</span></span> <span data-ttu-id="aa617-112">Temel uygulamayla ilişkili özellikleri güncelleştirmek için lütfen Update-AzADApplication cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="aa617-112">To update the properties associated with the underlying application, please use Update-AzADApplication cmdlet.</span></span>

## <span data-ttu-id="aa617-113">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="aa617-113">EXAMPLES</span></span>

### <span data-ttu-id="aa617-114">Örnek 1: hizmet sorumlusunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="aa617-114">Example 1: Update the display name of a service principal</span></span>

```powershell
PS C:\> Update-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 -DisplayName MyNewDisplayName
```

<span data-ttu-id="aa617-115">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunun görünen adını ' Yenisdisplayname ' olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aa617-115">Updates the display name of the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' to be 'MyNewDisplayName'.</span></span>

### <span data-ttu-id="aa617-116">Örnek 2: yöneltme kullanarak hizmet sorumlusunun görünen adını güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="aa617-116">Example 2: Update the display name of a service principal using piping</span></span>

```powershell
PS C:\> Get-AzADServicePrincipal -ObjectId 784136ca-3ae2-4fdd-a388-89d793e7c780 | Update-AzADServicePrincipal -DisplayName MyNewDisplayName
```

<span data-ttu-id="aa617-117">' 784136ca-3ae2-4fdd-A388-89r793e7c780 ' ile hizmet sorumlusunu ve hizmet sorumlusunun görünen adını "Yenisör" olarak güncelleştirmek için Update-AzADServicePrincipal cmdlet 'ine sahip kanalları alır.</span><span class="sxs-lookup"><span data-stu-id="aa617-117">Gets the service principal with object id '784136ca-3ae2-4fdd-a388-89d793e7c780' and pipes that to the Update-AzADServicePrincipal cmdlet to update the display name of the service principal to "MyNewDisplayName".</span></span>

### <span data-ttu-id="aa617-118">Örnek 3</span><span class="sxs-lookup"><span data-stu-id="aa617-118">Example 3</span></span>

<span data-ttu-id="aa617-119">Var olan bir Azure Active Directory hizmet sorumlusunu güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="aa617-119">Updates an existing azure active directory service principal.</span></span> <span data-ttu-id="aa617-120">oluşturulmuş</span><span class="sxs-lookup"><span data-stu-id="aa617-120">(autogenerated)</span></span>

<!-- Aladdin Generated Example -->
```powershell
Update-AzADServicePrincipal -IdentifierUri https://mySecretApp1 -ObjectId 00000000-0000-0000-0000-00000000000000000
```

## <span data-ttu-id="aa617-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="aa617-121">PARAMETERS</span></span>

### <span data-ttu-id="aa617-122">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="aa617-122">-ApplicationId</span></span>
<span data-ttu-id="aa617-123">Güncelleştirilecek hizmet sorumlusunun uygulama kimliği.</span><span class="sxs-lookup"><span data-stu-id="aa617-123">The application id of the service principal to update.</span></span>

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

### <span data-ttu-id="aa617-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="aa617-124">-DefaultProfile</span></span>
<span data-ttu-id="aa617-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="aa617-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="aa617-126">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="aa617-126">-DisplayName</span></span>
<span data-ttu-id="aa617-127">Hizmet sorumlusunun görünen adı.</span><span class="sxs-lookup"><span data-stu-id="aa617-127">The display name for the service principal.</span></span>

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

### <span data-ttu-id="aa617-128">-Giriş sayfası</span><span class="sxs-lookup"><span data-stu-id="aa617-128">-Homepage</span></span>
<span data-ttu-id="aa617-129">Hizmet sorumlusu için ana sayfa.</span><span class="sxs-lookup"><span data-stu-id="aa617-129">The homepage for the service principal.</span></span>

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

### <span data-ttu-id="aa617-130">-Identifieruri</span><span class="sxs-lookup"><span data-stu-id="aa617-130">-IdentifierUri</span></span>
<span data-ttu-id="aa617-131">Hizmet sorumlusunun tanımlayıcı URI 'leri.</span><span class="sxs-lookup"><span data-stu-id="aa617-131">The identifier URI(s) for the service principal.</span></span>

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

### <span data-ttu-id="aa617-132">-InputObject</span><span class="sxs-lookup"><span data-stu-id="aa617-132">-InputObject</span></span>
<span data-ttu-id="aa617-133">Güncelleştirilecek hizmet sorumlusunu temsil eden nesne.</span><span class="sxs-lookup"><span data-stu-id="aa617-133">The object representing the service principal to update.</span></span>

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

### <span data-ttu-id="aa617-134">-KeyCredential</span><span class="sxs-lookup"><span data-stu-id="aa617-134">-KeyCredential</span></span>
<span data-ttu-id="aa617-135">Hizmet sorumlusu için anahtar kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="aa617-135">The key credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="aa617-136">-ObjectID</span><span class="sxs-lookup"><span data-stu-id="aa617-136">-ObjectId</span></span>
<span data-ttu-id="aa617-137">Güncelleştirilecek hizmet sorumlusunun nesne kimliği.</span><span class="sxs-lookup"><span data-stu-id="aa617-137">The object id of the service principal to update.</span></span>

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

### <span data-ttu-id="aa617-138">-PasswordCredential</span><span class="sxs-lookup"><span data-stu-id="aa617-138">-PasswordCredential</span></span>
<span data-ttu-id="aa617-139">Hizmet sorumlusunun parola kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="aa617-139">The password credential(s) for the service principal.</span></span>

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

### <span data-ttu-id="aa617-140">-ServicePrincipalName</span><span class="sxs-lookup"><span data-stu-id="aa617-140">-ServicePrincipalName</span></span>
<span data-ttu-id="aa617-141">Güncelleştirilecek hizmet sorumlusunun SPN 'si.</span><span class="sxs-lookup"><span data-stu-id="aa617-141">The SPN of the service principal to update.</span></span>

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

### <span data-ttu-id="aa617-142">-Onay</span><span class="sxs-lookup"><span data-stu-id="aa617-142">-Confirm</span></span>
<span data-ttu-id="aa617-143">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="aa617-143">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="aa617-144">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="aa617-144">-WhatIf</span></span>
<span data-ttu-id="aa617-145">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="aa617-145">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="aa617-146">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="aa617-146">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="aa617-147">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="aa617-147">CommonParameters</span></span>
<span data-ttu-id="aa617-148">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="aa617-148">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="aa617-149">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="aa617-149">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="aa617-150">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="aa617-150">INPUTS</span></span>

### <span data-ttu-id="aa617-151">System. String</span><span class="sxs-lookup"><span data-stu-id="aa617-151">System.String</span></span>

### <span data-ttu-id="aa617-152">System. Guid</span><span class="sxs-lookup"><span data-stu-id="aa617-152">System.Guid</span></span>

### <span data-ttu-id="aa617-153">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aa617-153">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="aa617-154">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="aa617-154">OUTPUTS</span></span>

### <span data-ttu-id="aa617-155">Microsoft. Azure. Commands. ActiveDirectory. PSADServicePrincipal</span><span class="sxs-lookup"><span data-stu-id="aa617-155">Microsoft.Azure.Commands.ActiveDirectory.PSADServicePrincipal</span></span>

## <span data-ttu-id="aa617-156">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="aa617-156">NOTES</span></span>

## <span data-ttu-id="aa617-157">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="aa617-157">RELATED LINKS</span></span>

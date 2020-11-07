---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Add-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 4c0f576d118a502b04d4effd9a1de8f98e2a3813
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933167"
---
# <span data-ttu-id="f3a11-101">Add-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="f3a11-101">Add-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="f3a11-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f3a11-102">SYNOPSIS</span></span>
<span data-ttu-id="f3a11-103">Sağlanan yönetilen örneğe bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-103">Adds a key vault key to the provided Managed Instance.</span></span> 

## <span data-ttu-id="f3a11-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f3a11-104">SYNTAX</span></span>

### <span data-ttu-id="f3a11-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="f3a11-105">AddAzureRmSqlInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a11-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3a11-106">AddAzureRmSqlInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="f3a11-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="f3a11-107">AddAzureRmSqlInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Add-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="f3a11-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="f3a11-108">DESCRIPTION</span></span>
<span data-ttu-id="f3a11-109">Add-AzSqlInstanceKeyVaultKey cmdlet 'i, sağlanan yönetilen örneğe bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-109">The Add-AzSqlInstanceKeyVaultKey cmdlet adds a key vault key to the provided Managed Instance.</span></span> <span data-ttu-id="f3a11-110">Yönetilen örnekte kasaya ' Get, wrapKey, unwrapKey ' izinleri olmalıdır, yönetilen örneğe izin vermek için aşağıdaki komut dosyasını kullanın.</span><span class="sxs-lookup"><span data-stu-id="f3a11-110">The managed instance must have 'get, wrapKey, unwrapKey' permissions to the vault, use the following script to grant permission to the managed instance.</span></span>
<span data-ttu-id="f3a11-111">$managedInstance = Get-AzSqlInstance-Name ' Contosomanagedınstancename '-ResourceGroupName ' ContosoResourceGroup ' Set-AzKeyVaultAccessPolicy-VaultName Contosokasa-ObjectID $managedInstance. Identity. PrincipalId-PermissionsToKeys Get, wrapKey, unwrapKey</span><span class="sxs-lookup"><span data-stu-id="f3a11-111">$managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup' Set-AzKeyVaultAccessPolicy -VaultName ContosoVault -ObjectId $managedInstance.Identity.PrincipalId -PermissionsToKeys get, wrapKey, unwrapKey</span></span>

## <span data-ttu-id="f3a11-112">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f3a11-112">EXAMPLES</span></span>

### <span data-ttu-id="f3a11-113">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f3a11-113">Example 1</span></span>
```powershell
PS C:\> Add-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3a11-114">Bu komut, ' ', ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' Contosomanagedınstancename ' ADLı SQL yönetilen örneğine kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-114">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3a11-115">Örnek 2: yönetilen örnek nesnesini kullanma</span><span class="sxs-lookup"><span data-stu-id="f3a11-115">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3a11-116">Bu komut, ' ', ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' Contosomanagedınstancename ' ADLı SQL yönetilen örneğine kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-116">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3a11-117">Örnek 3: yönetilen örnek kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="f3a11-117">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Add-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3a11-118">Bu komut, ' ', ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' Contosomanagedınstancename ' ADLı SQL yönetilen örneğine kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-118">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

### <span data-ttu-id="f3a11-119">Örnek 4: boru kullanma</span><span class="sxs-lookup"><span data-stu-id="f3a11-119">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Add-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="f3a11-120">Bu komut, ' ', ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' Contosomanagedınstancename ' ADLı SQL yönetilen örneğine kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="f3a11-120">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL managed instance named 'ContosoManagedInstanceName' in the resource group 'ContosoResourceGroup'.</span></span> 

## <span data-ttu-id="f3a11-121">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f3a11-121">PARAMETERS</span></span>

### <span data-ttu-id="f3a11-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f3a11-122">-DefaultProfile</span></span>
<span data-ttu-id="f3a11-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f3a11-123">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="f3a11-124">-Örnek</span><span class="sxs-lookup"><span data-stu-id="f3a11-124">-Instance</span></span>
<span data-ttu-id="f3a11-125">Örnek giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="f3a11-125">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a11-126">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="f3a11-126">-InstanceName</span></span>
<span data-ttu-id="f3a11-127">Örnek adı</span><span class="sxs-lookup"><span data-stu-id="f3a11-127">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a11-128">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="f3a11-128">-InstanceResourceId</span></span>
<span data-ttu-id="f3a11-129">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="f3a11-129">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="f3a11-130">-KeyId</span><span class="sxs-lookup"><span data-stu-id="f3a11-130">-KeyId</span></span>
<span data-ttu-id="f3a11-131">AzureKeyVault anahtar kimliği</span><span class="sxs-lookup"><span data-stu-id="f3a11-131">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a11-132">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="f3a11-132">-ResourceGroupName</span></span>
<span data-ttu-id="f3a11-133">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="f3a11-133">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f3a11-134">-Onay</span><span class="sxs-lookup"><span data-stu-id="f3a11-134">-Confirm</span></span>
<span data-ttu-id="f3a11-135">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="f3a11-135">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="f3a11-136">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="f3a11-136">-WhatIf</span></span>
<span data-ttu-id="f3a11-137">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="f3a11-137">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="f3a11-138">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="f3a11-138">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="f3a11-139">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f3a11-139">CommonParameters</span></span>
<span data-ttu-id="f3a11-140">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f3a11-140">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f3a11-141">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="f3a11-141">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f3a11-142">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f3a11-142">INPUTS</span></span>

### <span data-ttu-id="f3a11-143">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="f3a11-143">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="f3a11-144">System. String</span><span class="sxs-lookup"><span data-stu-id="f3a11-144">System.String</span></span>

## <span data-ttu-id="f3a11-145">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f3a11-145">OUTPUTS</span></span>

### <span data-ttu-id="f3a11-146">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="f3a11-146">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="f3a11-147">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f3a11-147">NOTES</span></span>

## <span data-ttu-id="f3a11-148">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f3a11-148">RELATED LINKS</span></span>

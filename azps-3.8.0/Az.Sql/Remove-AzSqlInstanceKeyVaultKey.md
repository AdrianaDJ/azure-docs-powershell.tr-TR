---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Remove-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Remove-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 6812f6da3e32fd6074dc6958568bf3bd7eddeff0
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94098424"
---
# <span data-ttu-id="47daa-101">Remove-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="47daa-101">Remove-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="47daa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="47daa-102">SYNOPSIS</span></span>
<span data-ttu-id="47daa-103">SQL yönetilen örneğinden bir anahtar kasa anahtarını kaldırır</span><span class="sxs-lookup"><span data-stu-id="47daa-103">Removes a Key Vault key from a SQL managed instance</span></span>

## <span data-ttu-id="47daa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="47daa-104">SYNTAX</span></span>

### <span data-ttu-id="47daa-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="47daa-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-ResourceGroupName] <String> [-InstanceName] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47daa-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="47daa-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-Instance] <AzureSqlManagedInstanceModel> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="47daa-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="47daa-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Remove-AzSqlInstanceKeyVaultKey [-InstanceResourceId] <String> [-KeyId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="47daa-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="47daa-108">DESCRIPTION</span></span>
<span data-ttu-id="47daa-109">Remove-AzSqlInstanceKeyVaultKey cmdlet 'i, belirtilen yönetilen örnekten anahtar kasa anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="47daa-109">The Remove-AzSqlInstanceKeyVaultKey cmdlet  removes the Key Vault key from the specified Managed Instance.</span></span> <span data-ttu-id="47daa-110">SQL yönetilen örneğinin Anahtar Kasası izinlerinin değiştirilmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="47daa-110">Note that the SQL managed instance's permissions to the key's vault are not changed.</span></span> <span data-ttu-id="47daa-111">İzinleri değiştirmek için set-AzKeyVaultAccessPolicy seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="47daa-111">To change permissions, use Set-AzKeyVaultAccessPolicy.</span></span> <span data-ttu-id="47daa-112">Bu cmdlet 'in anahtar kasada hiçbir değişiklik yapmaz.</span><span class="sxs-lookup"><span data-stu-id="47daa-112">Note that this cmdlet makes no changes to Key Vault.</span></span> <span data-ttu-id="47daa-113">Anahtar kasasından anahtar kaldırmak için Remove-AzureKeyVaultKey kullanın.</span><span class="sxs-lookup"><span data-stu-id="47daa-113">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="47daa-114">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="47daa-114">EXAMPLES</span></span>

### <span data-ttu-id="47daa-115">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="47daa-115">Example 1</span></span>
```powershell
PS C:\> Remove-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="47daa-116">Bu komut, belirtilen yönetilen örnekten kimliği ' ' olan Anahtar Kasası öğesini kaldırır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="47daa-116">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="47daa-117">Örnek 2: yönetilen örnek nesnesini kullanma</span><span class="sxs-lookup"><span data-stu-id="47daa-117">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -Instance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="47daa-118">Bu komut, belirtilen yönetilen örnekten kimliği ' ' olan Anahtar Kasası öğesini kaldırır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="47daa-118">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="47daa-119">Örnek 3: yönetilen örnek kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="47daa-119">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Remove-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="47daa-120">Bu komut, belirtilen yönetilen örnekten kimliği ' ' olan Anahtar Kasası öğesini kaldırır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="47daa-120">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

### <span data-ttu-id="47daa-121">Örnek 4: boru kullanma</span><span class="sxs-lookup"><span data-stu-id="47daa-121">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Remove-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="47daa-122">Bu komut, belirtilen yönetilen örnekten kimliği ' ' olan Anahtar Kasası öğesini kaldırır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="47daa-122">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified managed instance.</span></span> 

## <span data-ttu-id="47daa-123">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="47daa-123">PARAMETERS</span></span>

### <span data-ttu-id="47daa-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="47daa-124">-DefaultProfile</span></span>
<span data-ttu-id="47daa-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="47daa-125">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="47daa-126">-Örnek</span><span class="sxs-lookup"><span data-stu-id="47daa-126">-Instance</span></span>
<span data-ttu-id="47daa-127">Örnek giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="47daa-127">The instance input object</span></span>

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

### <span data-ttu-id="47daa-128">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="47daa-128">-InstanceName</span></span>
<span data-ttu-id="47daa-129">Örnek adı</span><span class="sxs-lookup"><span data-stu-id="47daa-129">The instance name</span></span>

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

### <span data-ttu-id="47daa-130">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="47daa-130">-InstanceResourceId</span></span>
<span data-ttu-id="47daa-131">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="47daa-131">The instance resource id</span></span>

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

### <span data-ttu-id="47daa-132">-KeyId</span><span class="sxs-lookup"><span data-stu-id="47daa-132">-KeyId</span></span>
<span data-ttu-id="47daa-133">AzureKeyVault anahtar kimliği</span><span class="sxs-lookup"><span data-stu-id="47daa-133">AzureKeyVault key id</span></span>

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

### <span data-ttu-id="47daa-134">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="47daa-134">-ResourceGroupName</span></span>
<span data-ttu-id="47daa-135">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="47daa-135">The Resource Group Name</span></span>

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

### <span data-ttu-id="47daa-136">-Onay</span><span class="sxs-lookup"><span data-stu-id="47daa-136">-Confirm</span></span>
<span data-ttu-id="47daa-137">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="47daa-137">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="47daa-138">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="47daa-138">-WhatIf</span></span>
<span data-ttu-id="47daa-139">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="47daa-139">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="47daa-140">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="47daa-140">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="47daa-141">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="47daa-141">CommonParameters</span></span>
<span data-ttu-id="47daa-142">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="47daa-142">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="47daa-143">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="47daa-143">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="47daa-144">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="47daa-144">INPUTS</span></span>

### <span data-ttu-id="47daa-145">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="47daa-145">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="47daa-146">System. String</span><span class="sxs-lookup"><span data-stu-id="47daa-146">System.String</span></span>

## <span data-ttu-id="47daa-147">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="47daa-147">OUTPUTS</span></span>

### <span data-ttu-id="47daa-148">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="47daa-148">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="47daa-149">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="47daa-149">NOTES</span></span>

## <span data-ttu-id="47daa-150">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="47daa-150">RELATED LINKS</span></span>

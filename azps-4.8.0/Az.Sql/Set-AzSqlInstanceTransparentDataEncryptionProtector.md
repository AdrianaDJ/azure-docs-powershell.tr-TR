---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Set-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 15462ea79b5499818d71b145e0faaa35c09baf0b
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94273870"
---
# <span data-ttu-id="6ba2f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="6ba2f-101">Set-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="6ba2f-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6ba2f-102">SYNOPSIS</span></span>
<span data-ttu-id="6ba2f-103">Bir SQL yönetilen örneği için saydam veri şifreleme (TDE) koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-103">Sets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="6ba2f-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6ba2f-104">SYNTAX</span></span>

### <span data-ttu-id="6ba2f-105">Azures, Rmmanagedınstancetransparentdataencryptionkorunabilir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="6ba2f-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ResourceGroupName] <String> [-InstanceName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba2f-106">Azuressınrmmanagedınstancetransparentdataencryptionkoruyucuinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="6ba2f-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-Instance] <AzureSqlManagedInstanceModel> [-DefaultProfile <IAzureContextContainer>] [-WhatIf]
 [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="6ba2f-107">Azures, Rmmanagedınstancetransparentdataencryptionkorunabilir</span><span class="sxs-lookup"><span data-stu-id="6ba2f-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Set-AzSqlInstanceTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-InstanceResourceId] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="6ba2f-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="6ba2f-108">DESCRIPTION</span></span>
<span data-ttu-id="6ba2f-109">Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet 'i bir SQL yönetilen örneğinin TDE koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-109">The Set-AzSqlInstanceTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL managed instance.</span></span> <span data-ttu-id="6ba2f-110">TDE koruyucu türü değiştirildiğinde, koruyucu döndürülür.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-110">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="6ba2f-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6ba2f-111">EXAMPLES</span></span>

### <span data-ttu-id="6ba2f-112">Örnek 1: saydam veri şifreleme (TDE) koruyucu türünü ServiceManaged olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba2f-112">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type ServiceManaged

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : ServiceManaged
ManagedInstanceKeyVaultKeyName : ServiceManaged
KeyId                          :
```

<span data-ttu-id="6ba2f-113">Bu komut yönetilen bir örneğin TDE koruyucu türünü hizmet yönetimli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-113">This command updates a managed instance's TDE protector type to Service Managed.</span></span>

### <span data-ttu-id="6ba2f-114">Örnek 2: saydam veri şifreleme koruyucusu türünü Azure Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba2f-114">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```powershell
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="6ba2f-115">Bu komut belirtilen yönetilen örneği, TDE koruyucusu olarak kimliği ' ' olan yönetilen örnek Anahtar Kasası kullanacak şekilde güncelleştirir https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="6ba2f-115">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="6ba2f-116">Örnek 3: yönetilen örnek nesnesini kullanarak saydam veri şifreleme koruyucusunu Azure Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba2f-116">Example 3: Set the Transparent Data Encryption protector type to Azure Key Vault using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="6ba2f-117">Bu komut belirtilen yönetilen örneği, TDE koruyucusu olarak kimliği ' ' olan yönetilen örnek Anahtar Kasası kullanacak şekilde güncelleştirir https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="6ba2f-117">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="6ba2f-118">Örnek 4: kaynak kimliğini kullanarak saydam veri şifreleme koruyucusu türünü Azure Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba2f-118">Example 4: Set the Transparent Data Encryption protector type to Azure Key Vault using resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Set-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="6ba2f-119">Bu komut belirtilen yönetilen örneği, TDE koruyucusu olarak kimliği ' ' olan yönetilen örnek Anahtar Kasası kullanacak şekilde güncelleştirir https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="6ba2f-119">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

### <span data-ttu-id="6ba2f-120">Örnek 5: boru kullanarak saydam veri şifreleme koruyucusu türünü Azure Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="6ba2f-120">Example 5: Set the Transparent Data Encryption protector type to Azure Key Vault using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Set-AzSqlInstanceTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="6ba2f-121">Bu komut belirtilen yönetilen örneği, TDE koruyucusu olarak kimliği ' ' olan yönetilen örnek Anahtar Kasası kullanacak şekilde güncelleştirir https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="6ba2f-121">This command updates the specified managed instance to use the Managed instance Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

## <span data-ttu-id="6ba2f-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6ba2f-122">PARAMETERS</span></span>

### <span data-ttu-id="6ba2f-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6ba2f-123">-DefaultProfile</span></span>
<span data-ttu-id="6ba2f-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6ba2f-125">-Force</span><span class="sxs-lookup"><span data-stu-id="6ba2f-125">-Force</span></span>
<span data-ttu-id="6ba2f-126">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="6ba2f-126">Skip confirmation message for performing the action</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-127">-Örnek</span><span class="sxs-lookup"><span data-stu-id="6ba2f-127">-Instance</span></span>
<span data-ttu-id="6ba2f-128">Örnek giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="6ba2f-128">The instance input object</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet
Aliases: InputObject

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-129">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="6ba2f-129">-InstanceName</span></span>
<span data-ttu-id="6ba2f-130">Örnek adı</span><span class="sxs-lookup"><span data-stu-id="6ba2f-130">The instance name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-131">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="6ba2f-131">-InstanceResourceId</span></span>
<span data-ttu-id="6ba2f-132">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="6ba2f-132">The instance resource id</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet
Aliases: ResourceId

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-133">-KeyId</span><span class="sxs-lookup"><span data-stu-id="6ba2f-133">-KeyId</span></span>
<span data-ttu-id="6ba2f-134">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-134">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-135">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6ba2f-135">-ResourceGroupName</span></span>
<span data-ttu-id="6ba2f-136">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="6ba2f-136">The Resource Group Name</span></span>

```yaml
Type: System.String
Parameter Sets: AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-137">-Tür</span><span class="sxs-lookup"><span data-stu-id="6ba2f-137">-Type</span></span>
<span data-ttu-id="6ba2f-138">Azure SQL veritabanı saydam veri şifreleme koruyucusu türü.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-138">The Azure Sql Database Transparent Data Encryption Protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6ba2f-139">-Onay</span><span class="sxs-lookup"><span data-stu-id="6ba2f-139">-Confirm</span></span>
<span data-ttu-id="6ba2f-140">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-140">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6ba2f-141">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6ba2f-141">-WhatIf</span></span>
<span data-ttu-id="6ba2f-142">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-142">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="6ba2f-143">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-143">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6ba2f-144">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6ba2f-144">CommonParameters</span></span>
<span data-ttu-id="6ba2f-145">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-145">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6ba2f-146">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6ba2f-146">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6ba2f-147">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6ba2f-147">INPUTS</span></span>

### <span data-ttu-id="6ba2f-148">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="6ba2f-148">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="6ba2f-149">System. String</span><span class="sxs-lookup"><span data-stu-id="6ba2f-149">System.String</span></span>

## <span data-ttu-id="6ba2f-150">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6ba2f-150">OUTPUTS</span></span>

### <span data-ttu-id="6ba2f-151">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. Azurermsqlmanagedınstancetransparentdataencryptionspartormodel</span><span class="sxs-lookup"><span data-stu-id="6ba2f-151">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="6ba2f-152">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6ba2f-152">NOTES</span></span>

## <span data-ttu-id="6ba2f-153">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6ba2f-153">RELATED LINKS</span></span>

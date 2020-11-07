---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceKeyVaultKey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceKeyVaultKey.md
ms.openlocfilehash: 8c17ca9f899adc731c549b45617c287010baaac5
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933891"
---
# <span data-ttu-id="17bea-101">Get-AzSqlInstanceKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="17bea-101">Get-AzSqlInstanceKeyVaultKey</span></span>

## <span data-ttu-id="17bea-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="17bea-102">SYNOPSIS</span></span>
<span data-ttu-id="17bea-103">SQL yönetilen örneğinin Anahtar Kasası anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="17bea-103">Gets a SQL managed instance's Key Vault keys.</span></span>

## <span data-ttu-id="17bea-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="17bea-104">SYNTAX</span></span>

### <span data-ttu-id="17bea-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="17bea-105">AddAzureRmSqlManagedInstanceKeyVaultKeyDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17bea-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span><span class="sxs-lookup"><span data-stu-id="17bea-106">AddAzureRmSqlManagedInstanceKeyVaultKeyInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="17bea-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span><span class="sxs-lookup"><span data-stu-id="17bea-107">AddAzureRmSqlManagedInstanceKeyVaultKeyResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceKeyVaultKey [[-KeyId] <String>] [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="17bea-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="17bea-108">DESCRIPTION</span></span>
<span data-ttu-id="17bea-109">Get-AzSqlInstanceKeyVaultKey cmdlet, SQL yönetilen örneğindeki anahtar kasa anahtarları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="17bea-109">The Get-AzSqlInstanceKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL managed instance.</span></span> <span data-ttu-id="17bea-110">Bir yönetilen örnekteki tüm tuşları görüntüleyebilir veya anahtar kimliği sağlayarak belirli bir anahtarı görebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="17bea-110">You can view all keys on a managed instance or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="17bea-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="17bea-111">EXAMPLES</span></span>

### <span data-ttu-id="17bea-112">Örnek 1: tüm önemli kasa anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="17bea-112">Example 1: Get all Key Vault keys</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="17bea-113">Bu komut, SQL yönetilen örneğindeki tüm önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="17bea-113">This command gets all the Key Vault keys on a SQL managed instance.</span></span>

### <span data-ttu-id="17bea-114">Örnek 2: belirli bir Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="17bea-114">Example 2: Get a specific Key Vault key</span></span>
```powershell
PS C:\> Get-AzSqlInstanceKeyVaultKey -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName' -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="17bea-115">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="17bea-115">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="17bea-116">Örnek 3: örnek nesne kullanma</span><span class="sxs-lookup"><span data-stu-id="17bea-116">Example 3: Using instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -ManagedInstance $managedInstance -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="17bea-117">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="17bea-117">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="17bea-118">Örnek 4: örnek kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="17bea-118">Example 4: Using instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceKeyVaultKey -InstanceResourceId $managedInstance.ResourceId -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="17bea-119">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="17bea-119">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

### <span data-ttu-id="17bea-120">Örnek 5: boru kullanma</span><span class="sxs-lookup"><span data-stu-id="17bea-120">Example 5: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'

ResourceGroupName      : ContosoResourceGroup
ManagedInstanceName    : ContosoManagedInstanceName
KeyId                  : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
ManagedInstanceKeyName : contoso_contosokey_01234567890123456789012345678901
CreationDate           : 9/1/2018 12:11:49 AM
Thumbprint             : 6AB10000F99E1B6A22222F39E3F11CB5DC5A55A1
Type                   : AzureKeyVault
```

<span data-ttu-id="17bea-121">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="17bea-121">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901'.</span></span>

## <span data-ttu-id="17bea-122">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="17bea-122">PARAMETERS</span></span>

### <span data-ttu-id="17bea-123">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="17bea-123">-DefaultProfile</span></span>
<span data-ttu-id="17bea-124">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="17bea-124">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="17bea-125">-Örnek</span><span class="sxs-lookup"><span data-stu-id="17bea-125">-Instance</span></span>
<span data-ttu-id="17bea-126">Örnek giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="17bea-126">The instance input object</span></span>

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

### <span data-ttu-id="17bea-127">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="17bea-127">-InstanceName</span></span>
<span data-ttu-id="17bea-128">Örnek adı</span><span class="sxs-lookup"><span data-stu-id="17bea-128">The instance name</span></span>

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

### <span data-ttu-id="17bea-129">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="17bea-129">-InstanceResourceId</span></span>
<span data-ttu-id="17bea-130">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="17bea-130">The instance resource id</span></span>

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

### <span data-ttu-id="17bea-131">-KeyId</span><span class="sxs-lookup"><span data-stu-id="17bea-131">-KeyId</span></span>
<span data-ttu-id="17bea-132">AzureKeyVault anahtar kimliği</span><span class="sxs-lookup"><span data-stu-id="17bea-132">AzureKeyVault key id</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 1
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="17bea-133">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="17bea-133">-ResourceGroupName</span></span>
<span data-ttu-id="17bea-134">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="17bea-134">The Resource Group Name</span></span>

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

### <span data-ttu-id="17bea-135">-Onay</span><span class="sxs-lookup"><span data-stu-id="17bea-135">-Confirm</span></span>
<span data-ttu-id="17bea-136">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="17bea-136">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="17bea-137">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="17bea-137">-WhatIf</span></span>
<span data-ttu-id="17bea-138">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="17bea-138">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="17bea-139">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="17bea-139">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="17bea-140">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="17bea-140">CommonParameters</span></span>
<span data-ttu-id="17bea-141">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="17bea-141">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="17bea-142">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="17bea-142">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="17bea-143">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="17bea-143">INPUTS</span></span>

### <span data-ttu-id="17bea-144">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="17bea-144">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="17bea-145">System. String</span><span class="sxs-lookup"><span data-stu-id="17bea-145">System.String</span></span>

## <span data-ttu-id="17bea-146">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="17bea-146">OUTPUTS</span></span>

### <span data-ttu-id="17bea-147">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureRmSqlManagedInstanceKeyVaultKeyModel</span><span class="sxs-lookup"><span data-stu-id="17bea-147">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceKeyVaultKeyModel</span></span>

## <span data-ttu-id="17bea-148">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="17bea-148">NOTES</span></span>

## <span data-ttu-id="17bea-149">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="17bea-149">RELATED LINKS</span></span>

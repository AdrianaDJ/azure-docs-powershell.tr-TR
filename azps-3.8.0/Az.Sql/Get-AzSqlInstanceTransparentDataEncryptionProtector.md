---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/Az.sql/Get-AzSqlInstanceTransparentDataEncryptionProtector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceTransparentDataEncryptionProtector.md
ms.openlocfilehash: 8307581d1e3627be5cb2ab9fc146327342ced187
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096063"
---
# <span data-ttu-id="c2fd0-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="c2fd0-101">Get-AzSqlInstanceTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="c2fd0-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c2fd0-102">SYNOPSIS</span></span>
<span data-ttu-id="c2fd0-103">Bir SQL yönetilen örneği için saydam veri şifreleme (TDE) koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-103">Gets the Transparent Data Encryption (TDE) protector for a SQL managed instance.</span></span>

## <span data-ttu-id="c2fd0-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c2fd0-104">SYNTAX</span></span>

### <span data-ttu-id="c2fd0-105">Azures, Rmmanagedınstancetransparentdataencryptionkorunabilir (varsayılan)</span><span class="sxs-lookup"><span data-stu-id="c2fd0-105">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorDefaultParameterSet (Default)</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-ResourceGroupName] <String> [-InstanceName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fd0-106">Azuressınrmmanagedınstancetransparentdataencryptionkoruyucuinputobjectparameterset</span><span class="sxs-lookup"><span data-stu-id="c2fd0-106">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorInputObjectParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-Instance] <AzureSqlManagedInstanceModel>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

### <span data-ttu-id="c2fd0-107">Azures, Rmmanagedınstancetransparentdataencryptionkorunabilir</span><span class="sxs-lookup"><span data-stu-id="c2fd0-107">AzureSqlRmManagedInstanceTransparentDataEncryptionProtectorResourceIdParameterSet</span></span>
```
Get-AzSqlInstanceTransparentDataEncryptionProtector [-InstanceResourceId] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c2fd0-108">Tanım</span><span class="sxs-lookup"><span data-stu-id="c2fd0-108">DESCRIPTION</span></span>
<span data-ttu-id="c2fd0-109">Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet 'i belirtilen SQL yönetilen örneğinin tın koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-109">The Get-AzSqlInstanceTransparentDataEncryptionProtector cmdlet gets the TDE protector for the specified SQL managed instance.</span></span>

## <span data-ttu-id="c2fd0-110">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c2fd0-110">EXAMPLES</span></span>

### <span data-ttu-id="c2fd0-111">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="c2fd0-111">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -ResourceGroupName 'ContosoResourceGroup' -InstanceName 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2fd0-112">Bu komut, ContosoResourceGroup adlı kaynak grubunda Contosomanagedınstancename adlı yönetilen örnek için TDE koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-112">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2fd0-113">Örnek 2: yönetilen örnek nesnesini kullanma</span><span class="sxs-lookup"><span data-stu-id="c2fd0-113">Example 2: Using managed instance object</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -Instance $managedInstance 'ContosoManagedInstanceName'

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2fd0-114">Bu komut, ContosoResourceGroup adlı kaynak grubunda Contosomanagedınstancename adlı yönetilen örnek için TDE koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-114">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2fd0-115">Örnek 3: yönetilen örnek kaynak kimliğini kullanma</span><span class="sxs-lookup"><span data-stu-id="c2fd0-115">Example 3: Using managed instance resource id</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> Get-AzSqlInstanceTransparentDataEncryptionProtector -InstanceResourceId $managedInstance.ResourceId

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2fd0-116">Bu komut, ContosoResourceGroup adlı kaynak grubunda Contosomanagedınstancename adlı yönetilen örnek için TDE koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-116">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

### <span data-ttu-id="c2fd0-117">Örnek 4: boru kullanma</span><span class="sxs-lookup"><span data-stu-id="c2fd0-117">Example 4: Using piping</span></span>
```powershell
PS C:\> $managedInstance = Get-AzSqlInstance -Name 'ContosoManagedInstanceName' -ResourceGroupName 'ContosoResourceGroup'
PS C:\> $managedInstance | Get-AzSqlInstanceTransparentDataEncryptionProtector

ResourceGroupName              : ContosoResourceGroup
ManagedInstanceName            : ContosoManagedInstanceName
Type                           : AzureKeyVault
ManagedInstanceKeyVaultKeyName : contoso_contosokey_01234567890123456789012345678901
KeyId                          : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901
```

<span data-ttu-id="c2fd0-118">Bu komut, ContosoResourceGroup adlı kaynak grubunda Contosomanagedınstancename adlı yönetilen örnek için TDE koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-118">This command gets the TDE protector for the managed instance named ContosoManagedInstanceName in resource group named ContosoResourceGroup.</span></span>

## <span data-ttu-id="c2fd0-119">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c2fd0-119">PARAMETERS</span></span>

### <span data-ttu-id="c2fd0-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c2fd0-120">-DefaultProfile</span></span>
<span data-ttu-id="c2fd0-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-121">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="c2fd0-122">-Örnek</span><span class="sxs-lookup"><span data-stu-id="c2fd0-122">-Instance</span></span>
<span data-ttu-id="c2fd0-123">Örnek giriş nesnesi</span><span class="sxs-lookup"><span data-stu-id="c2fd0-123">The instance input object</span></span>

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

### <span data-ttu-id="c2fd0-124">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="c2fd0-124">-InstanceName</span></span>
<span data-ttu-id="c2fd0-125">Örnek adı</span><span class="sxs-lookup"><span data-stu-id="c2fd0-125">The instance name</span></span>

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

### <span data-ttu-id="c2fd0-126">-Instanceresourceıd</span><span class="sxs-lookup"><span data-stu-id="c2fd0-126">-InstanceResourceId</span></span>
<span data-ttu-id="c2fd0-127">Örnek kaynak kimliği</span><span class="sxs-lookup"><span data-stu-id="c2fd0-127">The instance resource id</span></span>

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

### <span data-ttu-id="c2fd0-128">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c2fd0-128">-ResourceGroupName</span></span>
<span data-ttu-id="c2fd0-129">Kaynak grubu adı</span><span class="sxs-lookup"><span data-stu-id="c2fd0-129">The Resource Group Name</span></span>

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

### <span data-ttu-id="c2fd0-130">-Onay</span><span class="sxs-lookup"><span data-stu-id="c2fd0-130">-Confirm</span></span>
<span data-ttu-id="c2fd0-131">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-131">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c2fd0-132">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c2fd0-132">-WhatIf</span></span>
<span data-ttu-id="c2fd0-133">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-133">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c2fd0-134">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-134">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c2fd0-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c2fd0-135">CommonParameters</span></span>
<span data-ttu-id="c2fd0-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c2fd0-137">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c2fd0-137">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c2fd0-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c2fd0-138">INPUTS</span></span>

### <span data-ttu-id="c2fd0-139">Microsoft. Azure. Commands. Sql. ManagedInstance. model. Azureskalite Managedınstancemodel</span><span class="sxs-lookup"><span data-stu-id="c2fd0-139">Microsoft.Azure.Commands.Sql.ManagedInstance.Model.AzureSqlManagedInstanceModel</span></span>
<span data-ttu-id="c2fd0-140">System. String</span><span class="sxs-lookup"><span data-stu-id="c2fd0-140">System.String</span></span>

## <span data-ttu-id="c2fd0-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c2fd0-141">OUTPUTS</span></span>

### <span data-ttu-id="c2fd0-142">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. Azurermsqlmanagedınstancetransparentdataencryptionspartormodel</span><span class="sxs-lookup"><span data-stu-id="c2fd0-142">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureRmSqlManagedInstanceTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="c2fd0-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c2fd0-143">NOTES</span></span>

## <span data-ttu-id="c2fd0-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c2fd0-144">RELATED LINKS</span></span>
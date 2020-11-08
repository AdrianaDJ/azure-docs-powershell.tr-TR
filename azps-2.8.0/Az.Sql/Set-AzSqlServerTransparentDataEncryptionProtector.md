---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/set-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Set-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: d2d2bd98491b5bf91aebb45e6b8a3368a58d1b56
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933950"
---
# <span data-ttu-id="767a3-101">Set-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="767a3-101">Set-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="767a3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="767a3-102">SYNOPSIS</span></span>
<span data-ttu-id="767a3-103">SQL Server için saydam veri şifreleme (TDE) koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="767a3-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

## <span data-ttu-id="767a3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="767a3-104">SYNTAX</span></span>

```
Set-AzSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="767a3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="767a3-105">DESCRIPTION</span></span>
<span data-ttu-id="767a3-106">Set-AzSqlServerTransparentDataEncryptionProtector cmdlet 'i SQL Server 'ın TDE koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="767a3-106">The Set-AzSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="767a3-107">TDE koruyucu türü değiştirildiğinde, koruyucu döndürülür.</span><span class="sxs-lookup"><span data-stu-id="767a3-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="767a3-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="767a3-108">EXAMPLES</span></span>

### <span data-ttu-id="767a3-109">Örnek 1: saydam veri şifreleme (TDE) koruyucu türünü ServiceManaged olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="767a3-109">Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="767a3-110">Bu komut, sunucunun TDE koruyucu türünü hizmet yönetimli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="767a3-110">This command updates a server's TDE protector type to Service Managed.</span></span>
<span data-ttu-id="767a3-111">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="767a3-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="767a3-112">Contosocontoso</span><span class="sxs-lookup"><span data-stu-id="767a3-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="767a3-113">Örnek 2: saydam veri şifreleme koruyucusu türünü Azure Anahtar Kasası olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="767a3-113">Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault</span></span>
```
PS C:\> Set-AzSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="767a3-114">Bu komut https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 , sunucuyu, TDE koruyucusu olarak ' '</span><span class="sxs-lookup"><span data-stu-id="767a3-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>
<span data-ttu-id="767a3-115">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="767a3-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="767a3-116">Contosocontososerver AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="767a3-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="767a3-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="767a3-117">PARAMETERS</span></span>

### <span data-ttu-id="767a3-118">-Iş</span><span class="sxs-lookup"><span data-stu-id="767a3-118">-AsJob</span></span>
<span data-ttu-id="767a3-119">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="767a3-119">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="767a3-120">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="767a3-120">-DefaultProfile</span></span>
<span data-ttu-id="767a3-121">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="767a3-121">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="767a3-122">-Force</span><span class="sxs-lookup"><span data-stu-id="767a3-122">-Force</span></span>
<span data-ttu-id="767a3-123">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="767a3-123">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="767a3-124">-KeyId</span><span class="sxs-lookup"><span data-stu-id="767a3-124">-KeyId</span></span>
<span data-ttu-id="767a3-125">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="767a3-125">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-126">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="767a3-126">-ResourceGroupName</span></span>
<span data-ttu-id="767a3-127">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="767a3-127">The name of the resource group</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-128">-ServerName</span><span class="sxs-lookup"><span data-stu-id="767a3-128">-ServerName</span></span>
<span data-ttu-id="767a3-129">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="767a3-129">The Azure Sql Server name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-130">-Tür</span><span class="sxs-lookup"><span data-stu-id="767a3-130">-Type</span></span>
<span data-ttu-id="767a3-131">Azure SQL veritabanı TDE koruyucu türü.</span><span class="sxs-lookup"><span data-stu-id="767a3-131">The Azure Sql Database TDE protector type.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType
Parameter Sets: (All)
Aliases:
Accepted values: AzureKeyVault, ServiceManaged

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-132">-Onay</span><span class="sxs-lookup"><span data-stu-id="767a3-132">-Confirm</span></span>
<span data-ttu-id="767a3-133">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="767a3-133">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-134">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="767a3-134">-WhatIf</span></span>
<span data-ttu-id="767a3-135">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="767a3-135">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="767a3-136">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="767a3-136">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="767a3-137">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="767a3-137">CommonParameters</span></span>
<span data-ttu-id="767a3-138">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="767a3-138">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="767a3-139">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="767a3-139">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="767a3-140">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="767a3-140">INPUTS</span></span>

### <span data-ttu-id="767a3-141">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. Encryptionkorunabilir Tortype</span><span class="sxs-lookup"><span data-stu-id="767a3-141">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>

### <span data-ttu-id="767a3-142">System. String</span><span class="sxs-lookup"><span data-stu-id="767a3-142">System.String</span></span>

## <span data-ttu-id="767a3-143">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="767a3-143">OUTPUTS</span></span>

### <span data-ttu-id="767a3-144">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="767a3-144">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="767a3-145">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="767a3-145">NOTES</span></span>

## <span data-ttu-id="767a3-146">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="767a3-146">RELATED LINKS</span></span>

[<span data-ttu-id="767a3-147">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="767a3-147">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
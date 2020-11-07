---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Set-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: b13a09a018ff85a48dd2baf3cf8837950a325cfc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93765027"
---
# <span data-ttu-id="fda1c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="fda1c-101">Set-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="fda1c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fda1c-102">SYNOPSIS</span></span>
<span data-ttu-id="fda1c-103">SQL Server için saydam veri şifreleme (TDE) koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fda1c-103">Sets the Transparent Data Encryption (TDE) protector for a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fda1c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fda1c-104">SYNTAX</span></span>

```
Set-AzureRmSqlServerTransparentDataEncryptionProtector [-Type] <EncryptionProtectorType> [[-KeyId] <String>]
 [-Force] [-ServerName] <String> [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>]
 [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="fda1c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fda1c-105">DESCRIPTION</span></span>
<span data-ttu-id="fda1c-106">Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet 'i SQL Server 'ın TDE koruyucusunu ayarlar.</span><span class="sxs-lookup"><span data-stu-id="fda1c-106">The Set-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet sets the TDE protector for a SQL server.</span></span>
<span data-ttu-id="fda1c-107">TDE koruyucu türü değiştirildiğinde, koruyucu döndürülür.</span><span class="sxs-lookup"><span data-stu-id="fda1c-107">Changing the TDE protector type will rotate the protector.</span></span>

## <span data-ttu-id="fda1c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fda1c-108">EXAMPLES</span></span>

### <span data-ttu-id="fda1c-109">--------------------------Örnek 1: saydam veri şifreleme (TDE) koruyucu türünü ServiceManaged--------------------------olarak ayarlama</span><span class="sxs-lookup"><span data-stu-id="fda1c-109">--------------------------  Example 1: Set the Transparent Data Encryption (TDE) protector type to ServiceManaged  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type ServiceManaged -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="fda1c-110">Bu komut, sunucunun TDE koruyucu türünü hizmet yönetimli olarak güncelleştirir.</span><span class="sxs-lookup"><span data-stu-id="fda1c-110">This command updates a server's TDE protector type to Service Managed.</span></span>

<span data-ttu-id="fda1c-111">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="fda1c-111">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="fda1c-112">Contosocontoso</span><span class="sxs-lookup"><span data-stu-id="fda1c-112">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

### <span data-ttu-id="fda1c-113">--------------------------Örnek 2: saydam veri şifreleme koruyucusu türünü Azure Anahtar Kasası olarak ayarlama--------------------------</span><span class="sxs-lookup"><span data-stu-id="fda1c-113">--------------------------  Example 2: Set the Transparent Data Encryption protector type to Azure Key Vault  --------------------------</span></span>
```
PS C:\> Set-AzureRmSqlServerTransparentDataEncryptionProtector -Type AzureKeyVault -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="fda1c-114">Bu komut https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 , sunucuyu, TDE koruyucusu olarak ' '</span><span class="sxs-lookup"><span data-stu-id="fda1c-114">This command updates a server to use the Server Key Vault Key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' as the TDE protector.</span></span>

<span data-ttu-id="fda1c-115">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="fda1c-115">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="fda1c-116">Contosocontososerver AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span><span class="sxs-lookup"><span data-stu-id="fda1c-116">ContosoResourceGroup ContosoServer AzureKeyVault contoso_contosokey_01234567890123456789012345678901</span></span>

## <span data-ttu-id="fda1c-117">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fda1c-117">PARAMETERS</span></span>

### <span data-ttu-id="fda1c-118">-Force</span><span class="sxs-lookup"><span data-stu-id="fda1c-118">-Force</span></span>
<span data-ttu-id="fda1c-119">Eylemi gerçekleştirmek için onay iletisini atla</span><span class="sxs-lookup"><span data-stu-id="fda1c-119">Skip confirmation message for performing the action</span></span>

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

### <span data-ttu-id="fda1c-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="fda1c-120">-KeyId</span></span>
<span data-ttu-id="fda1c-121">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="fda1c-121">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="fda1c-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fda1c-122">-ResourceGroupName</span></span>
<span data-ttu-id="fda1c-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="fda1c-123">The name of the resource group</span></span>

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

### <span data-ttu-id="fda1c-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fda1c-124">-ServerName</span></span>
<span data-ttu-id="fda1c-125">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="fda1c-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="fda1c-126">-Tür</span><span class="sxs-lookup"><span data-stu-id="fda1c-126">-Type</span></span>
<span data-ttu-id="fda1c-127">Azure SQL veritabanı TDE koruyucu türü.</span><span class="sxs-lookup"><span data-stu-id="fda1c-127">The Azure Sql Database TDE protector type.</span></span>

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

### <span data-ttu-id="fda1c-128">-Onay</span><span class="sxs-lookup"><span data-stu-id="fda1c-128">-Confirm</span></span>
<span data-ttu-id="fda1c-129">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="fda1c-129">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="fda1c-130">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="fda1c-130">-WhatIf</span></span>
<span data-ttu-id="fda1c-131">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="fda1c-131">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="fda1c-132">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="fda1c-132">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="fda1c-133">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fda1c-133">-DefaultProfile</span></span>
<span data-ttu-id="fda1c-134">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="fda1c-134">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="fda1c-135">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fda1c-135">CommonParameters</span></span>
<span data-ttu-id="fda1c-136">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fda1c-136">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fda1c-137">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fda1c-137">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fda1c-138">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fda1c-138">INPUTS</span></span>

### <span data-ttu-id="fda1c-139">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. Encryptionkorunabilir Tortype</span><span class="sxs-lookup"><span data-stu-id="fda1c-139">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.EncryptionProtectorType</span></span>
<span data-ttu-id="fda1c-140">System. String</span><span class="sxs-lookup"><span data-stu-id="fda1c-140">System.String</span></span>

## <span data-ttu-id="fda1c-141">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fda1c-141">OUTPUTS</span></span>

### <span data-ttu-id="fda1c-142">System. Object</span><span class="sxs-lookup"><span data-stu-id="fda1c-142">System.Object</span></span>

## <span data-ttu-id="fda1c-143">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fda1c-143">NOTES</span></span>

## <span data-ttu-id="fda1c-144">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fda1c-144">RELATED LINKS</span></span>

[<span data-ttu-id="fda1c-145">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="fda1c-145">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

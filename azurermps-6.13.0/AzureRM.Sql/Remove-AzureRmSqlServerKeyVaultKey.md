---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/remove-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Remove-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 81ec18dd543a63a971d01a64c878774b266cf0fa
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594335"
---
# <span data-ttu-id="16d95-101">Remove-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="16d95-101">Remove-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="16d95-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="16d95-102">SYNOPSIS</span></span>
<span data-ttu-id="16d95-103">SQL sunucusundan bir anahtar kasa anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16d95-103">Removes a Key Vault key from a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="16d95-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="16d95-104">SYNTAX</span></span>

```
Remove-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="16d95-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="16d95-105">DESCRIPTION</span></span>
<span data-ttu-id="16d95-106">Remove-AzureRmSqlServerKeyVaultKey cmdlet 'i belirtilen SQL Server 'dan anahtar kasa anahtarını kaldırır.</span><span class="sxs-lookup"><span data-stu-id="16d95-106">The Remove-AzureRmSqlServerKeyVaultKey cmdlet removes the Key Vault key from the specified SQL server.</span></span>
<span data-ttu-id="16d95-107">SQL Server 'ın Anahtar Kasası izinleri değiştirilmediğini unutmayın.</span><span class="sxs-lookup"><span data-stu-id="16d95-107">Note that the SQL server's permissions to the key's vault are not changed.</span></span>
<span data-ttu-id="16d95-108">İzinleri değiştirmek için set-AzureRmKeyVaultAccessPolicy seçeneğini kullanın.</span><span class="sxs-lookup"><span data-stu-id="16d95-108">To change permissions, use Set-AzureRmKeyVaultAccessPolicy.</span></span>
<span data-ttu-id="16d95-109">Bu cmdlet 'in anahtar kasada hiçbir değişiklik yapmaz.</span><span class="sxs-lookup"><span data-stu-id="16d95-109">Note that this cmdlet makes no changes to Key Vault.</span></span>
<span data-ttu-id="16d95-110">Anahtar kasasından anahtar kaldırmak için Remove-AzureKeyVaultKey kullanın.</span><span class="sxs-lookup"><span data-stu-id="16d95-110">To remove a key from Key Vault, use Remove-AzureKeyVaultKey.</span></span>

## <span data-ttu-id="16d95-111">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="16d95-111">EXAMPLES</span></span>

### <span data-ttu-id="16d95-112">Örnek 1: anahtar kasa anahtarını kaldırma</span><span class="sxs-lookup"><span data-stu-id="16d95-112">Example 1: Remove a Key Vault key</span></span>
```
PS C:\> Remove-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="16d95-113">Bu komut, belirtilen sunucudan kimliği ' ' olan Anahtar Kasası anahtarını kaldırır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 .</span><span class="sxs-lookup"><span data-stu-id="16d95-113">This command removes the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' from the specified server.</span></span>
<span data-ttu-id="16d95-114">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="16d95-114">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="16d95-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="16d95-115">PARAMETERS</span></span>

### <span data-ttu-id="16d95-116">-Iş</span><span class="sxs-lookup"><span data-stu-id="16d95-116">-AsJob</span></span>
<span data-ttu-id="16d95-117">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="16d95-117">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="16d95-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="16d95-118">-DefaultProfile</span></span>
<span data-ttu-id="16d95-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="16d95-119">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="16d95-120">-KeyId</span><span class="sxs-lookup"><span data-stu-id="16d95-120">-KeyId</span></span>
<span data-ttu-id="16d95-121">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="16d95-121">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="16d95-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="16d95-122">-ResourceGroupName</span></span>
<span data-ttu-id="16d95-123">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="16d95-123">The name of the resource group</span></span>

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

### <span data-ttu-id="16d95-124">-ServerName</span><span class="sxs-lookup"><span data-stu-id="16d95-124">-ServerName</span></span>
<span data-ttu-id="16d95-125">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="16d95-125">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="16d95-126">-Onay</span><span class="sxs-lookup"><span data-stu-id="16d95-126">-Confirm</span></span>
<span data-ttu-id="16d95-127">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="16d95-127">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="16d95-128">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="16d95-128">-WhatIf</span></span>
<span data-ttu-id="16d95-129">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="16d95-129">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="16d95-130">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="16d95-130">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="16d95-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="16d95-131">CommonParameters</span></span>
<span data-ttu-id="16d95-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="16d95-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="16d95-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="16d95-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="16d95-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="16d95-134">INPUTS</span></span>

### <span data-ttu-id="16d95-135">System. String</span><span class="sxs-lookup"><span data-stu-id="16d95-135">System.String</span></span>

## <span data-ttu-id="16d95-136">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="16d95-136">OUTPUTS</span></span>

### <span data-ttu-id="16d95-137">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel</span><span class="sxs-lookup"><span data-stu-id="16d95-137">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="16d95-138">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="16d95-138">NOTES</span></span>

## <span data-ttu-id="16d95-139">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="16d95-139">RELATED LINKS</span></span>

[<span data-ttu-id="16d95-140">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="16d95-140">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

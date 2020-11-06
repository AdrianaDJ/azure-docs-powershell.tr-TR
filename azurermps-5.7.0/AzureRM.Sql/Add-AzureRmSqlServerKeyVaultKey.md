---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/add-azurermsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: bf82ca7804ecd3f382728217395be234155e9035
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589667"
---
# <span data-ttu-id="ede3a-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="ede3a-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="ede3a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="ede3a-102">SYNOPSIS</span></span>
<span data-ttu-id="ede3a-103">SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="ede3a-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="ede3a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="ede3a-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="ede3a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="ede3a-105">DESCRIPTION</span></span>
<span data-ttu-id="ede3a-106">Add-AzureRmSqlServerKeyVaultKey cmdlet 'i, sağlanan SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="ede3a-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="ede3a-107">Sunucuda kasaya ' Get, wrapKey, unwrapKey ' izinleri bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="ede3a-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="ede3a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="ede3a-108">EXAMPLES</span></span>

### <span data-ttu-id="ede3a-109">Örnek 1: Anahtar Kasası ekleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="ede3a-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="ede3a-110">Bu komut, ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' ContosoServer ' ADLı SQL sunucusuna kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="ede3a-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="ede3a-111">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="ede3a-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="ede3a-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="ede3a-112">PARAMETERS</span></span>

### <span data-ttu-id="ede3a-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="ede3a-113">-AsJob</span></span>
<span data-ttu-id="ede3a-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="ede3a-114">Run cmdlet in the background</span></span>
```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="ede3a-115">-DefaultProfile</span></span>
<span data-ttu-id="ede3a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="ede3a-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="ede3a-117">-KeyId</span></span>
<span data-ttu-id="ede3a-118">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="ede3a-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="ede3a-119">-ResourceGroupName</span></span>
<span data-ttu-id="ede3a-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="ede3a-120">The name of the resource group</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="ede3a-121">-ServerName</span></span>
<span data-ttu-id="ede3a-122">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="ede3a-122">The Azure Sql Server name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="ede3a-123">-Confirm</span></span>
<span data-ttu-id="ede3a-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="ede3a-124">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="ede3a-125">-WhatIf</span></span>
<span data-ttu-id="ede3a-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="ede3a-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="ede3a-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="ede3a-127">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: False
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="ede3a-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="ede3a-128">CommonParameters</span></span>
<span data-ttu-id="ede3a-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="ede3a-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="ede3a-130">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="ede3a-130">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="ede3a-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="ede3a-131">INPUTS</span></span>

### <span data-ttu-id="ede3a-132">System. String</span><span class="sxs-lookup"><span data-stu-id="ede3a-132">System.String</span></span>

## <span data-ttu-id="ede3a-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="ede3a-133">OUTPUTS</span></span>

### <span data-ttu-id="ede3a-134">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel</span><span class="sxs-lookup"><span data-stu-id="ede3a-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="ede3a-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="ede3a-135">NOTES</span></span>

## <span data-ttu-id="ede3a-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="ede3a-136">RELATED LINKS</span></span>

[<span data-ttu-id="ede3a-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="ede3a-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

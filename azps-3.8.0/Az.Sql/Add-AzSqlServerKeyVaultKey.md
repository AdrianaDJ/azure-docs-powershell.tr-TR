---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/add-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Add-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: f207726741155b22b16f8e69638c86eab684c658
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096745"
---
# <span data-ttu-id="c6de5-101">Add-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="c6de5-101">Add-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="c6de5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="c6de5-102">SYNOPSIS</span></span>
<span data-ttu-id="c6de5-103">SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="c6de5-103">Adds a Key Vault key to a SQL server.</span></span>

## <span data-ttu-id="c6de5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="c6de5-104">SYNTAX</span></span>

```
Add-AzSqlServerKeyVaultKey [-KeyId] <String> [-AsJob] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="c6de5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="c6de5-105">DESCRIPTION</span></span>
<span data-ttu-id="c6de5-106">Add-AzSqlServerKeyVaultKey cmdlet 'i, sağlanan SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="c6de5-106">The Add-AzSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="c6de5-107">Sunucuda kasaya ' Get, wrapKey, unwrapKey ' izinleri bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="c6de5-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="c6de5-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="c6de5-108">EXAMPLES</span></span>

### <span data-ttu-id="c6de5-109">Örnek 1: Anahtar Kasası ekleme anahtarı</span><span class="sxs-lookup"><span data-stu-id="c6de5-109">Example 1: Add Key Vault key</span></span>
```
PS C:\> Add-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="c6de5-110">Bu komut, ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' ContosoServer ' ADLı SQL sunucusuna kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="c6de5-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>
<span data-ttu-id="c6de5-111">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="c6de5-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="c6de5-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="c6de5-112">PARAMETERS</span></span>

### <span data-ttu-id="c6de5-113">-Iş</span><span class="sxs-lookup"><span data-stu-id="c6de5-113">-AsJob</span></span>
<span data-ttu-id="c6de5-114">Arka planda cmdlet 'i çalıştırın</span><span class="sxs-lookup"><span data-stu-id="c6de5-114">Run cmdlet in the background</span></span>

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

### <span data-ttu-id="c6de5-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="c6de5-115">-DefaultProfile</span></span>
<span data-ttu-id="c6de5-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="c6de5-116">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="c6de5-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="c6de5-117">-KeyId</span></span>
<span data-ttu-id="c6de5-118">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="c6de5-118">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="c6de5-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="c6de5-119">-ResourceGroupName</span></span>
<span data-ttu-id="c6de5-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="c6de5-120">The name of the resource group</span></span>

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

### <span data-ttu-id="c6de5-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="c6de5-121">-ServerName</span></span>
<span data-ttu-id="c6de5-122">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="c6de5-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="c6de5-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="c6de5-123">-Confirm</span></span>
<span data-ttu-id="c6de5-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="c6de5-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="c6de5-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="c6de5-125">-WhatIf</span></span>
<span data-ttu-id="c6de5-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="c6de5-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="c6de5-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="c6de5-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="c6de5-128">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="c6de5-128">CommonParameters</span></span>
<span data-ttu-id="c6de5-129">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="c6de5-129">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="c6de5-130">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="c6de5-130">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="c6de5-131">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="c6de5-131">INPUTS</span></span>

### <span data-ttu-id="c6de5-132">System. String</span><span class="sxs-lookup"><span data-stu-id="c6de5-132">System.String</span></span>

## <span data-ttu-id="c6de5-133">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="c6de5-133">OUTPUTS</span></span>

### <span data-ttu-id="c6de5-134">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel</span><span class="sxs-lookup"><span data-stu-id="c6de5-134">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="c6de5-135">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="c6de5-135">NOTES</span></span>

## <span data-ttu-id="c6de5-136">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="c6de5-136">RELATED LINKS</span></span>

[<span data-ttu-id="c6de5-137">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="c6de5-137">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)
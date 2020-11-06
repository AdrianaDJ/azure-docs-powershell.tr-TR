---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Add-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: b9051f8729ae1cee8216de5d2dab6d5ceb79a717
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594556"
---
# <span data-ttu-id="af884-101">Add-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="af884-101">Add-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="af884-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="af884-102">SYNOPSIS</span></span>
<span data-ttu-id="af884-103">SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="af884-103">Adds a Key Vault key to a SQL server.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="af884-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="af884-104">SYNTAX</span></span>

```
Add-AzureRmSqlServerKeyVaultKey [-KeyId] <String> [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="af884-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="af884-105">DESCRIPTION</span></span>
<span data-ttu-id="af884-106">Add-AzureRmSqlServerKeyVaultKey cmdlet 'i, sağlanan SQL sunucusuna bir anahtar kasa anahtarı ekler.</span><span class="sxs-lookup"><span data-stu-id="af884-106">The Add-AzureRmSqlServerKeyVaultKey cmdlet adds a Key Vault key to the provided SQL server.</span></span>
<span data-ttu-id="af884-107">Sunucuda kasaya ' Get, wrapKey, unwrapKey ' izinleri bulunmalıdır.</span><span class="sxs-lookup"><span data-stu-id="af884-107">The server must have 'get, wrapKey, unwrapKey' permissions to the vault.</span></span>

## <span data-ttu-id="af884-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="af884-108">EXAMPLES</span></span>

### <span data-ttu-id="af884-109">--------------------------Örnek 1: anahtar kasa anahtarı ekleme--------------------------</span><span class="sxs-lookup"><span data-stu-id="af884-109">--------------------------  Example 1: Add Key Vault key  --------------------------</span></span>
```
PS C:\> Add-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="af884-110">Bu komut, ' https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ' ' ContosoResourceGroup ' kaynak grubunda ' ContosoServer ' ADLı SQL sunucusuna kimliği ' ' olan Anahtar Kasası anahtarını ekler.</span><span class="sxs-lookup"><span data-stu-id="af884-110">This command adds the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' to the SQL server named 'ContosoServer' in the resource group 'ContosoResourceGroup'.</span></span>

<span data-ttu-id="af884-111">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="af884-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

## <span data-ttu-id="af884-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="af884-112">PARAMETERS</span></span>

### <span data-ttu-id="af884-113">-KeyId</span><span class="sxs-lookup"><span data-stu-id="af884-113">-KeyId</span></span>
<span data-ttu-id="af884-114">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="af884-114">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="af884-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="af884-115">-ResourceGroupName</span></span>
<span data-ttu-id="af884-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="af884-116">The name of the resource group</span></span>

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

### <span data-ttu-id="af884-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="af884-117">-ServerName</span></span>
<span data-ttu-id="af884-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="af884-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="af884-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="af884-119">-Confirm</span></span>
<span data-ttu-id="af884-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="af884-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="af884-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="af884-121">-WhatIf</span></span>
<span data-ttu-id="af884-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="af884-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="af884-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="af884-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="af884-124">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="af884-124">-DefaultProfile</span></span>
<span data-ttu-id="af884-125">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="af884-125">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="af884-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="af884-126">CommonParameters</span></span>
<span data-ttu-id="af884-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="af884-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="af884-128">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="af884-128">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="af884-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="af884-129">INPUTS</span></span>

### <span data-ttu-id="af884-130">System. String</span><span class="sxs-lookup"><span data-stu-id="af884-130">System.String</span></span>

## <span data-ttu-id="af884-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="af884-131">OUTPUTS</span></span>

### <span data-ttu-id="af884-132">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel</span><span class="sxs-lookup"><span data-stu-id="af884-132">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="af884-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="af884-133">NOTES</span></span>

## <span data-ttu-id="af884-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="af884-134">RELATED LINKS</span></span>

[<span data-ttu-id="af884-135">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="af884-135">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

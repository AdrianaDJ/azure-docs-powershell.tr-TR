---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerKeyVaultKey.md
ms.openlocfilehash: 17022a34ad8a5f2be673243e9dcb6c7063c8fbcc
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93589039"
---
# <span data-ttu-id="db2c9-101">Get-AzureRmSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="db2c9-101">Get-AzureRmSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="db2c9-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="db2c9-102">SYNOPSIS</span></span>
<span data-ttu-id="db2c9-103">SQL Server 'ın tuş Kasası anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="db2c9-103">Gets a SQL server's Key Vault keys.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="db2c9-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="db2c9-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="db2c9-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="db2c9-105">DESCRIPTION</span></span>
<span data-ttu-id="db2c9-106">Get-AzureRmSqlServerKeyVaultKey cmdlet, SQL Server 'daki Anahtar Kasası anahtarları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="db2c9-106">The Get-AzureRmSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="db2c9-107">Bir sunucudaki tüm tuşları görüntüleyebilir veya anahtar kimliği sağlayarak belirli bir anahtarı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db2c9-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="db2c9-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="db2c9-108">EXAMPLES</span></span>

### <span data-ttu-id="db2c9-109">--------------------------Örnek 1: tüm tuş Kasası anahtarlarını alma--------------------------</span><span class="sxs-lookup"><span data-stu-id="db2c9-109">--------------------------  Example 1: Get all Key Vault keys  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="db2c9-110">Bu komut, SQL Server 'daki tüm önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="db2c9-110">This command gets all the Key Vault keys on a SQL server.</span></span>

<span data-ttu-id="db2c9-111">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="db2c9-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

<span data-ttu-id="db2c9-112">ResourceGroupName: ContosoResourceGroup sunucuadı sunucuadı: ContosoServer Sunucukeyname: contoso_contosokey2_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 parmak izi: 0099887766554433221100998877665544332211 CreationDate: 1/1/2017 12:00:00</span><span class="sxs-lookup"><span data-stu-id="db2c9-112">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="db2c9-113">--------------------------Örnek 2: belirli bir Anahtar Kasası--------------------------</span><span class="sxs-lookup"><span data-stu-id="db2c9-113">--------------------------  Example 2: Get a specific Key Vault key  --------------------------</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzureRmSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="db2c9-114">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ve $MyServerKeyVaultKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="db2c9-114">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="db2c9-115">Anahtar Kasası hakkındaki ayrıntıları almak için $MyServerKeyVaultKey özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="db2c9-115">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="db2c9-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="db2c9-116">PARAMETERS</span></span>

### <span data-ttu-id="db2c9-117">-KeyId</span><span class="sxs-lookup"><span data-stu-id="db2c9-117">-KeyId</span></span>
<span data-ttu-id="db2c9-118">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="db2c9-118">The Azure Key Vault KeyId.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="db2c9-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="db2c9-119">-ResourceGroupName</span></span>
<span data-ttu-id="db2c9-120">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="db2c9-120">The name of the resource group</span></span>

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

### <span data-ttu-id="db2c9-121">-ServerName</span><span class="sxs-lookup"><span data-stu-id="db2c9-121">-ServerName</span></span>
<span data-ttu-id="db2c9-122">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="db2c9-122">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="db2c9-123">-Onay</span><span class="sxs-lookup"><span data-stu-id="db2c9-123">-Confirm</span></span>
<span data-ttu-id="db2c9-124">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="db2c9-124">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="db2c9-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="db2c9-125">-WhatIf</span></span>
<span data-ttu-id="db2c9-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="db2c9-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="db2c9-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="db2c9-127">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="db2c9-128">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="db2c9-128">-DefaultProfile</span></span>
<span data-ttu-id="db2c9-129">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="db2c9-129">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="db2c9-130">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="db2c9-130">CommonParameters</span></span>
<span data-ttu-id="db2c9-131">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="db2c9-131">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="db2c9-132">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="db2c9-132">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="db2c9-133">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="db2c9-133">INPUTS</span></span>

### <span data-ttu-id="db2c9-134">System. String</span><span class="sxs-lookup"><span data-stu-id="db2c9-134">System.String</span></span>

## <span data-ttu-id="db2c9-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="db2c9-135">OUTPUTS</span></span>

### <span data-ttu-id="db2c9-136">System. Object</span><span class="sxs-lookup"><span data-stu-id="db2c9-136">System.Object</span></span>

## <span data-ttu-id="db2c9-137">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="db2c9-137">NOTES</span></span>

## <span data-ttu-id="db2c9-138">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="db2c9-138">RELATED LINKS</span></span>

[<span data-ttu-id="db2c9-139">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="db2c9-139">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

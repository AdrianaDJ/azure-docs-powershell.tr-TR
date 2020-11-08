---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlserverkeyvaultkey
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerKeyVaultKey.md
ms.openlocfilehash: 93e8e4a5bb45fce59e10b6fdde37f2bd6122f2fd
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94103702"
---
# <span data-ttu-id="0a60c-101">Get-AzSqlServerKeyVaultKey</span><span class="sxs-lookup"><span data-stu-id="0a60c-101">Get-AzSqlServerKeyVaultKey</span></span>

## <span data-ttu-id="0a60c-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0a60c-102">SYNOPSIS</span></span>
<span data-ttu-id="0a60c-103">SQL Server 'ın tuş Kasası anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0a60c-103">Gets a SQL server's Key Vault keys.</span></span>

## <span data-ttu-id="0a60c-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0a60c-104">SYNTAX</span></span>

```
Get-AzSqlServerKeyVaultKey [[-KeyId] <String>] [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0a60c-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0a60c-105">DESCRIPTION</span></span>
<span data-ttu-id="0a60c-106">Get-AzSqlServerKeyVaultKey cmdlet, SQL Server 'daki Anahtar Kasası anahtarları hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0a60c-106">The Get-AzSqlServerKeyVaultKey cmdlet gets information about the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="0a60c-107">Bir sunucudaki tüm tuşları görüntüleyebilir veya anahtar kimliği sağlayarak belirli bir anahtarı görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a60c-107">You can view all keys on a server or view a specific key by providing the KeyId.</span></span>

## <span data-ttu-id="0a60c-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0a60c-108">EXAMPLES</span></span>

### <span data-ttu-id="0a60c-109">Örnek 1: tüm önemli kasa anahtarlarını alma</span><span class="sxs-lookup"><span data-stu-id="0a60c-109">Example 1: Get all Key Vault keys</span></span>
```
PS C:\> Get-AzSqlServerKeyVaultKey -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="0a60c-110">Bu komut, SQL Server 'daki tüm önemli kasa anahtarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="0a60c-110">This command gets all the Key Vault keys on a SQL server.</span></span>
<span data-ttu-id="0a60c-111">ResourceGroupName: ContosoResourceGroup sunucuadı \ sunucuadı: Contososunucu Sunucukeyname: contoso_contosokey_01234567890123456789012345678901 tür: AzureKeyVault Uri: https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 parmak izi: 1122334455667788990011223344556677889900 CreationDate: 1/1/2017 12:00:00. Kaynakgrupadı: ContosoResourceGroup ServerName: ContosoServer Sunucukeyname 1/1/2017 12:00:00 contoso_contosokey2_01234567890123456789012345678901: https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109</span><span class="sxs-lookup"><span data-stu-id="0a60c-111">ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 Thumbprint        : 1122334455667788990011223344556677889900 CreationDate      : 1/1/2017 12:00:00 AM ResourceGroupName : ContosoResourceGroup ServerName        : ContosoServer ServerKeyName     : contoso_contosokey2_01234567890123456789012345678901 Type              : AzureKeyVault Uri               : https://contoso.vault.azure.net/keys/contosokey2/09876543210987654321098765432109 Thumbprint        : 0099887766554433221100998877665544332211 CreationDate      : 1/1/2017 12:00:00 AM</span></span>

### <span data-ttu-id="0a60c-112">Örnek 2: belirli bir Anahtar Kasası</span><span class="sxs-lookup"><span data-stu-id="0a60c-112">Example 2: Get a specific Key Vault key</span></span>
```
PS C:\> $MyServerKeyVaultKey = Get-AzSqlServerKeyVaultKey -KeyId 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901' -ServerName 'ContosoServer' -ResourceGroupName 'ContosoResourceGroup'
```

<span data-ttu-id="0a60c-113">Bu komut, kimliği ' ' olan Anahtar Kasası anahtarını alır https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901 ve $MyServerKeyVaultKey değişkeninde depolar.</span><span class="sxs-lookup"><span data-stu-id="0a60c-113">This command gets the Key Vault key with Id 'https://contoso.vault.azure.net/keys/contosokey/01234567890123456789012345678901', and then stores it in the $MyServerKeyVaultKey variable.</span></span>
<span data-ttu-id="0a60c-114">Anahtar Kasası hakkındaki ayrıntıları almak için $MyServerKeyVaultKey özelliklerini inceleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0a60c-114">You can inspect the properties of $MyServerKeyVaultKey to get details about the key vault.</span></span>

## <span data-ttu-id="0a60c-115">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0a60c-115">PARAMETERS</span></span>

### <span data-ttu-id="0a60c-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0a60c-116">-DefaultProfile</span></span>
<span data-ttu-id="0a60c-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="0a60c-117">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="0a60c-118">-KeyId</span><span class="sxs-lookup"><span data-stu-id="0a60c-118">-KeyId</span></span>
<span data-ttu-id="0a60c-119">Azure Anahtar Kasası tuş kimliği.</span><span class="sxs-lookup"><span data-stu-id="0a60c-119">The Azure Key Vault KeyId.</span></span>

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

### <span data-ttu-id="0a60c-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0a60c-120">-ResourceGroupName</span></span>
<span data-ttu-id="0a60c-121">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0a60c-121">The name of the resource group</span></span>

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

### <span data-ttu-id="0a60c-122">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0a60c-122">-ServerName</span></span>
<span data-ttu-id="0a60c-123">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="0a60c-123">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0a60c-124">-Onay</span><span class="sxs-lookup"><span data-stu-id="0a60c-124">-Confirm</span></span>
<span data-ttu-id="0a60c-125">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0a60c-125">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0a60c-126">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0a60c-126">-WhatIf</span></span>
<span data-ttu-id="0a60c-127">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0a60c-127">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0a60c-128">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0a60c-128">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0a60c-129">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0a60c-129">CommonParameters</span></span>
<span data-ttu-id="0a60c-130">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0a60c-130">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0a60c-131">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0a60c-131">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0a60c-132">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0a60c-132">INPUTS</span></span>

### <span data-ttu-id="0a60c-133">System. String</span><span class="sxs-lookup"><span data-stu-id="0a60c-133">System.String</span></span>

## <span data-ttu-id="0a60c-134">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0a60c-134">OUTPUTS</span></span>

### <span data-ttu-id="0a60c-135">Microsoft. Azure. Commands. Sql. ServerKeyVaultKey. model. azures, Serverkeyvaultkeymodel</span><span class="sxs-lookup"><span data-stu-id="0a60c-135">Microsoft.Azure.Commands.Sql.ServerKeyVaultKey.Model.AzureSqlServerKeyVaultKeyModel</span></span>

## <span data-ttu-id="0a60c-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0a60c-136">NOTES</span></span>

## <span data-ttu-id="0a60c-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0a60c-137">RELATED LINKS</span></span>

[<span data-ttu-id="0a60c-138">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0a60c-138">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 93ab4c51882a4c274fd10727d83f5507c7cfa583
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587144"
---
# <span data-ttu-id="542f2-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="542f2-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="542f2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="542f2-102">SYNOPSIS</span></span>
<span data-ttu-id="542f2-103">Saydam veri şifreleme (TDE) koruyucusunu alır</span><span class="sxs-lookup"><span data-stu-id="542f2-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="542f2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="542f2-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="542f2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="542f2-105">DESCRIPTION</span></span>
<span data-ttu-id="542f2-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet 'i, TDE koruyucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="542f2-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="542f2-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="542f2-107">EXAMPLES</span></span>

### <span data-ttu-id="542f2-108">Örnek 1: saydam veri şifreleme (TDE) koruyucusunu alma</span><span class="sxs-lookup"><span data-stu-id="542f2-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="542f2-109">Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoServer adlı sunucunun TDA koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="542f2-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="542f2-110">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="542f2-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="542f2-111">Contosocontoso</span><span class="sxs-lookup"><span data-stu-id="542f2-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="542f2-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="542f2-112">PARAMETERS</span></span>

### <span data-ttu-id="542f2-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="542f2-113">-DefaultProfile</span></span>
<span data-ttu-id="542f2-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="542f2-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="542f2-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="542f2-115">-ResourceGroupName</span></span>
<span data-ttu-id="542f2-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="542f2-116">The name of the resource group</span></span>

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

### <span data-ttu-id="542f2-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="542f2-117">-ServerName</span></span>
<span data-ttu-id="542f2-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="542f2-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="542f2-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="542f2-119">-Confirm</span></span>
<span data-ttu-id="542f2-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="542f2-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="542f2-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="542f2-121">-WhatIf</span></span>
<span data-ttu-id="542f2-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="542f2-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="542f2-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="542f2-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="542f2-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="542f2-124">CommonParameters</span></span>
<span data-ttu-id="542f2-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="542f2-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="542f2-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="542f2-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="542f2-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="542f2-127">INPUTS</span></span>

### <span data-ttu-id="542f2-128">System. String</span><span class="sxs-lookup"><span data-stu-id="542f2-128">System.String</span></span>

## <span data-ttu-id="542f2-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="542f2-129">OUTPUTS</span></span>

### <span data-ttu-id="542f2-130">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="542f2-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="542f2-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="542f2-131">NOTES</span></span>

## <span data-ttu-id="542f2-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="542f2-132">RELATED LINKS</span></span>

[<span data-ttu-id="542f2-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="542f2-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

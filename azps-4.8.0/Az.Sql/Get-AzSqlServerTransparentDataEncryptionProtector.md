---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlservertransparentdataencryptionprotector
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: a2920eb845a162ac83f41e5c8de8c47848485431
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94267598"
---
# <span data-ttu-id="a5ba1-101">Get-AzSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="a5ba1-101">Get-AzSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="a5ba1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a5ba1-102">SYNOPSIS</span></span>
<span data-ttu-id="a5ba1-103">Saydam veri şifreleme (TDE) koruyucusunu alır</span><span class="sxs-lookup"><span data-stu-id="a5ba1-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

## <span data-ttu-id="a5ba1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a5ba1-104">SYNTAX</span></span>

```
Get-AzSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="a5ba1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a5ba1-105">DESCRIPTION</span></span>
<span data-ttu-id="a5ba1-106">Get-AzSqlServerTransparentDataEncryptionProtector cmdlet 'i, TDE koruyucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-106">The Get-AzSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="a5ba1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a5ba1-107">EXAMPLES</span></span>

### <span data-ttu-id="a5ba1-108">Örnek 1: saydam veri şifreleme (TDE) koruyucusunu alma</span><span class="sxs-lookup"><span data-stu-id="a5ba1-108">Example 1: Get the Transparent Data Encryption (TDE) protector</span></span>
```
PS C:\> Get-AzSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="a5ba1-109">Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoServer adlı sunucunun TDA koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>
<span data-ttu-id="a5ba1-110">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="a5ba1-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="a5ba1-111">Contosocontoso</span><span class="sxs-lookup"><span data-stu-id="a5ba1-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="a5ba1-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a5ba1-112">PARAMETERS</span></span>

### <span data-ttu-id="a5ba1-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a5ba1-113">-DefaultProfile</span></span>
<span data-ttu-id="a5ba1-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="a5ba1-114">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="a5ba1-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a5ba1-115">-ResourceGroupName</span></span>
<span data-ttu-id="a5ba1-116">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="a5ba1-116">The name of the resource group</span></span>

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

### <span data-ttu-id="a5ba1-117">-ServerName</span><span class="sxs-lookup"><span data-stu-id="a5ba1-117">-ServerName</span></span>
<span data-ttu-id="a5ba1-118">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-118">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="a5ba1-119">-Onay</span><span class="sxs-lookup"><span data-stu-id="a5ba1-119">-Confirm</span></span>
<span data-ttu-id="a5ba1-120">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-120">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="a5ba1-121">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="a5ba1-121">-WhatIf</span></span>
<span data-ttu-id="a5ba1-122">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-122">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="a5ba1-123">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-123">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="a5ba1-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a5ba1-124">CommonParameters</span></span>
<span data-ttu-id="a5ba1-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a5ba1-126">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="a5ba1-126">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a5ba1-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a5ba1-127">INPUTS</span></span>

### <span data-ttu-id="a5ba1-128">System. String</span><span class="sxs-lookup"><span data-stu-id="a5ba1-128">System.String</span></span>

## <span data-ttu-id="a5ba1-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a5ba1-129">OUTPUTS</span></span>

### <span data-ttu-id="a5ba1-130">Microsoft. Azure. Commands. Sql. TransparentDataEncryption. model. AzureSqlServerTransparentDataEncryptionProtectorModel</span><span class="sxs-lookup"><span data-stu-id="a5ba1-130">Microsoft.Azure.Commands.Sql.TransparentDataEncryption.Model.AzureSqlServerTransparentDataEncryptionProtectorModel</span></span>

## <span data-ttu-id="a5ba1-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a5ba1-131">NOTES</span></span>

## <span data-ttu-id="a5ba1-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a5ba1-132">RELATED LINKS</span></span>

[<span data-ttu-id="a5ba1-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="a5ba1-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlServerTransparentDataEncryptionProtector.md
ms.openlocfilehash: 174bccd7b682c1c4922a5ca7b6bbfbd406667df0
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93587769"
---
# <span data-ttu-id="0f860-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span><span class="sxs-lookup"><span data-stu-id="0f860-101">Get-AzureRmSqlServerTransparentDataEncryptionProtector</span></span>

## <span data-ttu-id="0f860-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0f860-102">SYNOPSIS</span></span>
<span data-ttu-id="0f860-103">Saydam veri şifreleme (TDE) koruyucusunu alır</span><span class="sxs-lookup"><span data-stu-id="0f860-103">Gets the Transparent Data Encryption (TDE) protector</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="0f860-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0f860-104">SYNTAX</span></span>

```
Get-AzureRmSqlServerTransparentDataEncryptionProtector [-ServerName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="0f860-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0f860-105">DESCRIPTION</span></span>
<span data-ttu-id="0f860-106">Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet 'i, TDE koruyucusu hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="0f860-106">The Get-AzureRmSqlServerTransparentDataEncryptionProtector cmdlet gets information about the TDE protector.</span></span>

## <span data-ttu-id="0f860-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0f860-107">EXAMPLES</span></span>

### <span data-ttu-id="0f860-108">--------------------------Örnek 1: saydam veri şifreleme (TDE) koruyucusunu edinin--------------------------</span><span class="sxs-lookup"><span data-stu-id="0f860-108">--------------------------  Example 1: Get the Transparent Data Encryption (TDE) protector  --------------------------</span></span>
```
PS C:\> Get-AzureRmSqlServerTransparentDataEncryptionProtector -ServerName 'ContosoServer' -ResourceGroup 'ContosoResourceGroup'
```

<span data-ttu-id="0f860-109">Bu komut, ContosoResourceGroup adlı kaynak grubundaki ContosoServer adlı sunucunun TDA koruyucusunu alır.</span><span class="sxs-lookup"><span data-stu-id="0f860-109">This command gets the TDE protector for the server named ContosoServer in resource group named ContosoResourceGroup.</span></span>

<span data-ttu-id="0f860-110">ResourceGroupName sunucuadı tür Sunucuanahtarvaultanahtaradı</span><span class="sxs-lookup"><span data-stu-id="0f860-110">ResourceGroupName ServerName                   Type ServerKeyVaultKeyName</span></span>
----------------- ----------                   ---- ---------------------
<span data-ttu-id="0f860-111">Contosocontoso</span><span class="sxs-lookup"><span data-stu-id="0f860-111">ContosoResourceGroup ContosoServer ServiceManaged ServiceManaged</span></span>

## <span data-ttu-id="0f860-112">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0f860-112">PARAMETERS</span></span>

### <span data-ttu-id="0f860-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0f860-113">-ResourceGroupName</span></span>
<span data-ttu-id="0f860-114">Kaynak grubunun adı</span><span class="sxs-lookup"><span data-stu-id="0f860-114">The name of the resource group</span></span>

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

### <span data-ttu-id="0f860-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0f860-115">-ServerName</span></span>
<span data-ttu-id="0f860-116">Azure SQL Server adı.</span><span class="sxs-lookup"><span data-stu-id="0f860-116">The Azure Sql Server name.</span></span>

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

### <span data-ttu-id="0f860-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="0f860-117">-Confirm</span></span>
<span data-ttu-id="0f860-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="0f860-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="0f860-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="0f860-119">-WhatIf</span></span>
<span data-ttu-id="0f860-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="0f860-120">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="0f860-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="0f860-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="0f860-122">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0f860-122">-DefaultProfile</span></span>
<span data-ttu-id="0f860-123">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0f860-123">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="0f860-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0f860-124">CommonParameters</span></span>
<span data-ttu-id="0f860-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0f860-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0f860-126">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="0f860-126">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0f860-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0f860-127">INPUTS</span></span>

### <span data-ttu-id="0f860-128">System. String</span><span class="sxs-lookup"><span data-stu-id="0f860-128">System.String</span></span>

## <span data-ttu-id="0f860-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0f860-129">OUTPUTS</span></span>

### <span data-ttu-id="0f860-130">System. Object</span><span class="sxs-lookup"><span data-stu-id="0f860-130">System.Object</span></span>

## <span data-ttu-id="0f860-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0f860-131">NOTES</span></span>

## <span data-ttu-id="0f860-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0f860-132">RELATED LINKS</span></span>

[<span data-ttu-id="0f860-133">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="0f860-133">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

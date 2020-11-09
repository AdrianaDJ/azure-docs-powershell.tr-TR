---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: fe07416cd4c7ec9287937a405d8cfaf2a6111b23
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320438"
---
# <span data-ttu-id="f8e04-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="f8e04-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="f8e04-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="f8e04-102">SYNOPSIS</span></span>
<span data-ttu-id="f8e04-103">Geçiş için veritabanı kaynağını belirten Azure veritabanı geçiş hizmeti için Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8e04-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="f8e04-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="f8e04-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="f8e04-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="f8e04-105">DESCRIPTION</span></span>
<span data-ttu-id="f8e04-106">New-AzDataMigrationDatabaseInfo cmdlet, geçirilecek kaynak veritabanı örneğini belirten Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8e04-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="f8e04-107">Veritabanı adı giriş parametresi olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="f8e04-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="f8e04-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="f8e04-108">EXAMPLES</span></span>

### <span data-ttu-id="f8e04-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="f8e04-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="f8e04-110">Önceki örnek, kaynak veritabanı **AdventureWorks2016** için yeni bir databaseınfo nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="f8e04-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="f8e04-111">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="f8e04-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="f8e04-112">Get-AzSubscription cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="f8e04-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="f8e04-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="f8e04-113">PARAMETERS</span></span>

### <span data-ttu-id="f8e04-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="f8e04-114">-DefaultProfile</span></span>
<span data-ttu-id="f8e04-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="f8e04-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="f8e04-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="f8e04-116">-SourceDatabaseName</span></span>
<span data-ttu-id="f8e04-117">Kaynak veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="f8e04-117">Source Database Name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="f8e04-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="f8e04-118">CommonParameters</span></span>
<span data-ttu-id="f8e04-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="f8e04-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="f8e04-120">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="f8e04-120">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="f8e04-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="f8e04-121">INPUTS</span></span>

### <span data-ttu-id="f8e04-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="f8e04-122">None</span></span>

## <span data-ttu-id="f8e04-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="f8e04-123">OUTPUTS</span></span>

### <span data-ttu-id="f8e04-124">Microsoft. Azure. Management. DataMigration. modeller. Databaseınfo</span><span class="sxs-lookup"><span data-stu-id="f8e04-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="f8e04-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="f8e04-125">NOTES</span></span>

## <span data-ttu-id="f8e04-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="f8e04-126">RELATED LINKS</span></span>

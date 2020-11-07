---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationDatabaseInfo.md
ms.openlocfilehash: f1feead56c25b76890edd0fe183e65211294cf87
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93761037"
---
# <span data-ttu-id="b29f8-101">New-AzDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="b29f8-101">New-AzDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="b29f8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b29f8-102">SYNOPSIS</span></span>
<span data-ttu-id="b29f8-103">Geçiş için veritabanı kaynağını belirten Azure veritabanı geçiş hizmeti için Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b29f8-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

## <span data-ttu-id="b29f8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b29f8-104">SYNTAX</span></span>

```
New-AzDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="b29f8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b29f8-105">DESCRIPTION</span></span>
<span data-ttu-id="b29f8-106">New-AzDataMigrationDatabaseInfo cmdlet, geçirilecek kaynak veritabanı örneğini belirten Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b29f8-106">The New-AzDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="b29f8-107">Veritabanı adı giriş parametresi olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="b29f8-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="b29f8-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b29f8-108">EXAMPLES</span></span>

### <span data-ttu-id="b29f8-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="b29f8-109">Example 1</span></span>
```
PS C:\> New-AzDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="b29f8-110">Önceki örnek, kaynak veritabanı **AdventureWorks2016** için yeni bir databaseınfo nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="b29f8-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="b29f8-111">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="b29f8-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="b29f8-112">Get-AzSubscription cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="b29f8-112">You can confirm your login status by using the Get-AzSubscription cmdlet.</span></span>

## <span data-ttu-id="b29f8-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b29f8-113">PARAMETERS</span></span>

### <span data-ttu-id="b29f8-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b29f8-114">-DefaultProfile</span></span>
<span data-ttu-id="b29f8-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b29f8-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b29f8-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="b29f8-116">-SourceDatabaseName</span></span>
<span data-ttu-id="b29f8-117">Kaynak veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="b29f8-117">Source Database Name.</span></span>

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

### <span data-ttu-id="b29f8-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b29f8-118">CommonParameters</span></span>
<span data-ttu-id="b29f8-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b29f8-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b29f8-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b29f8-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b29f8-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b29f8-121">INPUTS</span></span>

### <span data-ttu-id="b29f8-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b29f8-122">None</span></span>

## <span data-ttu-id="b29f8-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b29f8-123">OUTPUTS</span></span>

### <span data-ttu-id="b29f8-124">Microsoft. Azure. Management. DataMigration. modeller. Databaseınfo</span><span class="sxs-lookup"><span data-stu-id="b29f8-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="b29f8-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b29f8-125">NOTES</span></span>

## <span data-ttu-id="b29f8-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b29f8-126">RELATED LINKS</span></span>

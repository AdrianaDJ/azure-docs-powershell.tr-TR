---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationDatabaseInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: c04a79a54e42c64fe897a419565e4816964879b6
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764968"
---
# <span data-ttu-id="9c77a-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="9c77a-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="9c77a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9c77a-102">SYNOPSIS</span></span>
<span data-ttu-id="9c77a-103">Geçiş için veritabanı kaynağını belirten Azure veritabanı geçiş hizmeti için Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c77a-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9c77a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9c77a-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9c77a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9c77a-105">DESCRIPTION</span></span>
<span data-ttu-id="9c77a-106">New-AzureRmDataMigrationDatabaseInfo cmdlet, geçirilecek kaynak veritabanı örneğini belirten Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c77a-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="9c77a-107">Veritabanı adı giriş parametresi olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="9c77a-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="9c77a-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9c77a-108">EXAMPLES</span></span>

### <span data-ttu-id="9c77a-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9c77a-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="9c77a-110">Önceki örnek, kaynak veritabanı **AdventureWorks2016** için yeni bir databaseınfo nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9c77a-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>
<span data-ttu-id="9c77a-111">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="9c77a-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="9c77a-112">Get-AzureSubscription cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="9c77a-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="9c77a-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9c77a-113">PARAMETERS</span></span>

### <span data-ttu-id="9c77a-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9c77a-114">-DefaultProfile</span></span>
<span data-ttu-id="9c77a-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9c77a-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9c77a-116">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="9c77a-116">-SourceDatabaseName</span></span>
<span data-ttu-id="9c77a-117">Kaynak veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="9c77a-117">Source Database Name.</span></span>

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

### <span data-ttu-id="9c77a-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9c77a-118">CommonParameters</span></span>
<span data-ttu-id="9c77a-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9c77a-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9c77a-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9c77a-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9c77a-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9c77a-121">INPUTS</span></span>

### <span data-ttu-id="9c77a-122">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9c77a-122">None</span></span>

## <span data-ttu-id="9c77a-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9c77a-123">OUTPUTS</span></span>

### <span data-ttu-id="9c77a-124">Microsoft. Azure. Management. DataMigration. modeller. Databaseınfo</span><span class="sxs-lookup"><span data-stu-id="9c77a-124">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>

## <span data-ttu-id="9c77a-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9c77a-125">NOTES</span></span>

## <span data-ttu-id="9c77a-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9c77a-126">RELATED LINKS</span></span>

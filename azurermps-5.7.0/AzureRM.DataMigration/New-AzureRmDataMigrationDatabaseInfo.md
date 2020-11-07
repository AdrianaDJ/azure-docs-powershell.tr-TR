---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationdatabaseinfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationDatabaseInfo.md
ms.openlocfilehash: 3b0729b07667e634f060293bd8593ed237606460
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764459"
---
# <span data-ttu-id="d8c08-101">New-AzureRmDataMigrationDatabaseInfo</span><span class="sxs-lookup"><span data-stu-id="d8c08-101">New-AzureRmDataMigrationDatabaseInfo</span></span>

## <span data-ttu-id="d8c08-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8c08-102">SYNOPSIS</span></span>
<span data-ttu-id="d8c08-103">Geçiş için veritabanı kaynağını belirten Azure veritabanı geçiş hizmeti için Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c08-103">Creates the DatabaseInfo object for the Azure Database Migration Service, which specifies the database source for migration.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="d8c08-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8c08-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName <String> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="d8c08-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8c08-105">DESCRIPTION</span></span>
<span data-ttu-id="d8c08-106">New-AzureRmDataMigrationDatabaseInfo cmdlet, geçirilecek kaynak veritabanı örneğini belirten Databaseınfo nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c08-106">The New-AzureRmDataMigrationDatabaseInfo cmdlet creates the DatabaseInfo object that specifies the source database instance to be migrated.</span></span> <span data-ttu-id="d8c08-107">Veritabanı adı giriş parametresi olarak alınır.</span><span class="sxs-lookup"><span data-stu-id="d8c08-107">Database name is taken in as input parameter.</span></span>

## <span data-ttu-id="d8c08-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8c08-108">EXAMPLES</span></span>

### <span data-ttu-id="d8c08-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8c08-109">Example 1</span></span>
```
PS C:\> New-AzureRmDataMigrationDatabaseInfo -SourceDatabaseName 'AdventureWorks2016'
```

<span data-ttu-id="d8c08-110">Önceki örnek, kaynak veritabanı **AdventureWorks2016** için yeni bir databaseınfo nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="d8c08-110">The preceding example creates a new DatabaseInfo object for the source database **AdventureWorks2016**.</span></span>

<span data-ttu-id="d8c08-111">Bu komut dosyası Azure hesabınızda oturum açtığınız varsayılır.</span><span class="sxs-lookup"><span data-stu-id="d8c08-111">This script assumes that you are already logged into your Azure account.</span></span> <span data-ttu-id="d8c08-112">Get-AzureSubscription cmdlet 'ini kullanarak oturum açma durumunuzu doğrulayabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="d8c08-112">You can confirm your login status by using the Get-AzureSubscription cmdlet.</span></span>

## <span data-ttu-id="d8c08-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8c08-113">PARAMETERS</span></span>

### <span data-ttu-id="d8c08-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8c08-114">-DefaultProfile</span></span>
<span data-ttu-id="d8c08-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8c08-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="d8c08-116">-Onay</span><span class="sxs-lookup"><span data-stu-id="d8c08-116">-Confirm</span></span>
<span data-ttu-id="d8c08-117">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="d8c08-117">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c08-118">-SourceDatabaseName</span><span class="sxs-lookup"><span data-stu-id="d8c08-118">-SourceDatabaseName</span></span>
<span data-ttu-id="d8c08-119">Kaynak veritabanı adı.</span><span class="sxs-lookup"><span data-stu-id="d8c08-119">Source Database Name.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: SourceDBName

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="d8c08-120">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="d8c08-120">-WhatIf</span></span>
<span data-ttu-id="d8c08-121">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="d8c08-121">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="d8c08-122">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="d8c08-122">The cmdlet is not run.</span></span>

```yaml
Type: SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="d8c08-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8c08-123">INPUTS</span></span>

### <span data-ttu-id="d8c08-124">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="d8c08-124">None</span></span>


## <span data-ttu-id="d8c08-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8c08-125">OUTPUTS</span></span>

### <span data-ttu-id="d8c08-126">Microsoft. Azure. Management. DataMigration. modeller. Databaseınfo</span><span class="sxs-lookup"><span data-stu-id="d8c08-126">Microsoft.Azure.Management.DataMigration.Models.DatabaseInfo</span></span>


## <span data-ttu-id="d8c08-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8c08-127">NOTES</span></span>

## <span data-ttu-id="d8c08-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8c08-128">RELATED LINKS</span></span>



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationConnectionInfo.md
ms.openlocfilehash: e902785745ab22ab9bc1386fc2c6a2f9dd416b79
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94320442"
---
# <span data-ttu-id="06ad6-101">New-AzDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="06ad6-101">New-AzDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="06ad6-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="06ad6-102">SYNOPSIS</span></span>
<span data-ttu-id="06ad6-103">Bağlantı için sunucu türünü ve adını belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06ad6-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

## <span data-ttu-id="06ad6-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="06ad6-104">SYNTAX</span></span>

```
New-AzDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="06ad6-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="06ad6-105">DESCRIPTION</span></span>
<span data-ttu-id="06ad6-106">New-AzDataMigrationConnectionInfo cmdlet, bağlantı için sunucu türünü belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06ad6-106">The New-AzDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="06ad6-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="06ad6-107">EXAMPLES</span></span>

### <span data-ttu-id="06ad6-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="06ad6-108">Example 1</span></span>
```
PS C:\> New-AzDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="06ad6-109">Önceki örnek, SQL as ServerType parametresi sağlayan yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="06ad6-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="06ad6-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="06ad6-110">PARAMETERS</span></span>

### <span data-ttu-id="06ad6-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="06ad6-111">-DefaultProfile</span></span>
<span data-ttu-id="06ad6-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="06ad6-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="06ad6-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="06ad6-113">-ServerType</span></span>
<span data-ttu-id="06ad6-114">Bağlanılacak sunucu türünü açıklayan Enum.</span><span class="sxs-lookup"><span data-stu-id="06ad6-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="06ad6-115">Şu anda desteklenen değerler SQL Server için SQL Server, Azure SQL yönetilen örneği, MongoDb, CosmosDb ve Azure SQL veritabanı.</span><span class="sxs-lookup"><span data-stu-id="06ad6-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance, MongoDb, CosmosDb and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL, MongoDb, SQLMI

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="06ad6-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="06ad6-116">CommonParameters</span></span>
<span data-ttu-id="06ad6-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="06ad6-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="06ad6-118">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="06ad6-118">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="06ad6-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="06ad6-119">INPUTS</span></span>

### <span data-ttu-id="06ad6-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="06ad6-120">None</span></span>

## <span data-ttu-id="06ad6-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="06ad6-121">OUTPUTS</span></span>

### <span data-ttu-id="06ad6-122">Microsoft. Azure. Management. DataMigration. modeller. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="06ad6-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="06ad6-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="06ad6-123">NOTES</span></span>

## <span data-ttu-id="06ad6-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="06ad6-124">RELATED LINKS</span></span>

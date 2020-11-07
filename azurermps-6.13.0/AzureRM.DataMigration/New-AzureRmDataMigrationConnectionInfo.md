---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/New-AzureRmDataMigrationConnectionInfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: 77559f5858c26d665d062f822a5c65258625bb14
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93762952"
---
# <span data-ttu-id="9a693-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="9a693-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="9a693-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9a693-102">SYNOPSIS</span></span>
<span data-ttu-id="9a693-103">Bağlantı için sunucu türünü ve adını belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a693-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="9a693-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9a693-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="9a693-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9a693-105">DESCRIPTION</span></span>
<span data-ttu-id="9a693-106">New-AzureRmDataMigrationConnectionInfo cmdlet, bağlantı için sunucu türünü belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a693-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 

## <span data-ttu-id="9a693-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9a693-107">EXAMPLES</span></span>

### <span data-ttu-id="9a693-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="9a693-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```

<span data-ttu-id="9a693-109">Önceki örnek, SQL as ServerType parametresi sağlayan yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="9a693-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>

## <span data-ttu-id="9a693-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9a693-110">PARAMETERS</span></span>

### <span data-ttu-id="9a693-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9a693-111">-DefaultProfile</span></span>
<span data-ttu-id="9a693-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9a693-112">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="9a693-113">-ServerType</span><span class="sxs-lookup"><span data-stu-id="9a693-113">-ServerType</span></span>
<span data-ttu-id="9a693-114">Bağlanılacak sunucu türünü açıklayan Enum.</span><span class="sxs-lookup"><span data-stu-id="9a693-114">Enum that describes server type to connect to.</span></span> <span data-ttu-id="9a693-115">Şu anda desteklenen değerler SQL Server için SQL Server, Azure SQL yönetilen örneği ve Azure SQL veritabanı.</span><span class="sxs-lookup"><span data-stu-id="9a693-115">Currently supported values are SQL for SQL Server, Azure SQL Managed Instance and Azure SQL Database.</span></span> 

```yaml
Type: Microsoft.Azure.Commands.DataMigration.Models.ServerTypeEnum
Parameter Sets: (All)
Aliases:
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9a693-116">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9a693-116">CommonParameters</span></span>
<span data-ttu-id="9a693-117">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9a693-117">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9a693-118">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9a693-118">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9a693-119">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9a693-119">INPUTS</span></span>

### <span data-ttu-id="9a693-120">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9a693-120">None</span></span>

## <span data-ttu-id="9a693-121">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9a693-121">OUTPUTS</span></span>

### <span data-ttu-id="9a693-122">Microsoft. Azure. Management. DataMigration. modeller. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="9a693-122">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>

## <span data-ttu-id="9a693-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9a693-123">NOTES</span></span>

## <span data-ttu-id="9a693-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9a693-124">RELATED LINKS</span></span>

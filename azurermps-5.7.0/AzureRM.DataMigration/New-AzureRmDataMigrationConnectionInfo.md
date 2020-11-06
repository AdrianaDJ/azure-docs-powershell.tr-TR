---
external help file: Microsoft.Azure.Commands.DataMigration.dll-Help.xml
Module Name: AzureRM.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.datamigration/new-azurermdatamigrationconnectioninfo
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/DataMigration/Commands.DataMigration/help/New-AzureRmDataMigrationConnectionInfo.md
ms.openlocfilehash: aca970403d7ef85733d808c8e21df3d0b2066f9c
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588217"
---
# <span data-ttu-id="21fa8-101">New-AzureRmDataMigrationConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="21fa8-101">New-AzureRmDataMigrationConnectionInfo</span></span>

## <span data-ttu-id="21fa8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="21fa8-102">SYNOPSIS</span></span>
<span data-ttu-id="21fa8-103">Bağlantı için sunucu türünü ve adını belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21fa8-103">Creates a new Connection Info object specifying the server type and name for connection.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="21fa8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="21fa8-104">SYNTAX</span></span>

```
New-AzureRmDataMigrationConnectionInfo -ServerType <ServerTypeEnum> [-DefaultProfile <IAzureContextContainer>]
```

## <span data-ttu-id="21fa8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="21fa8-105">DESCRIPTION</span></span>
<span data-ttu-id="21fa8-106">New-AzureRmDataMigrationConnectionInfo cmdlet, bağlantı için sunucu türünü belirten yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21fa8-106">The New-AzureRmDataMigrationConnectionInfo cmdlet creates new a Connection Info object specifying the server type for connection.</span></span> 



## <span data-ttu-id="21fa8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="21fa8-107">EXAMPLES</span></span>

### <span data-ttu-id="21fa8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="21fa8-108">Example 1</span></span>
```
PS C:\> New-AzureRmDmsConnInfo -ServerType SQL -DataSource mySourceServer -AuthType SqlAuthentication -TrustServerCertificate:$true
```
<span data-ttu-id="21fa8-109">Önceki örnek, SQL as ServerType parametresi sağlayan yeni bir bağlantı bilgileri nesnesi oluşturur.</span><span class="sxs-lookup"><span data-stu-id="21fa8-109">The preceding example creates a new Connection Info object providing SQL as ServerType parameter.</span></span>


## <span data-ttu-id="21fa8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="21fa8-110">PARAMETERS</span></span>

### <span data-ttu-id="21fa8-111">-Onay</span><span class="sxs-lookup"><span data-stu-id="21fa8-111">-Confirm</span></span>
<span data-ttu-id="21fa8-112">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="21fa8-112">Prompts you for confirmation before running the cmdlet.</span></span>

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
### <span data-ttu-id="21fa8-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="21fa8-113">-DefaultProfile</span></span>
<span data-ttu-id="21fa8-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="21fa8-114">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="21fa8-115">-ServerType</span><span class="sxs-lookup"><span data-stu-id="21fa8-115">-ServerType</span></span>
<span data-ttu-id="21fa8-116">Bağlanılacak sunucu türünü açıklayan Enum.</span><span class="sxs-lookup"><span data-stu-id="21fa8-116">Enum that describes server type to connect to.</span></span> <span data-ttu-id="21fa8-117">Şu anda desteklenen değerler SQL Server için SQL Server ve SQL Azure veritabanı için SQLDB.</span><span class="sxs-lookup"><span data-stu-id="21fa8-117">Currently supported values are SQL for SQL Server and SQLDB for SQL Azure Database.</span></span> 

```yaml
Type: ServerTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL, SQLDB

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```
### <span data-ttu-id="21fa8-118">-AuthType</span><span class="sxs-lookup"><span data-stu-id="21fa8-118">-AuthType</span></span>
<span data-ttu-id="21fa8-119">Bağlantı için kullanılacak kimlik doğrulama türü.</span><span class="sxs-lookup"><span data-stu-id="21fa8-119">Authentication type to use for connection.</span></span> <span data-ttu-id="21fa8-120">Olası değerler SqlAuthentication ve WindowsAuthentication</span><span class="sxs-lookup"><span data-stu-id="21fa8-120">Possible values are SqlAuthentication and WindowsAuthentication</span></span>

```yaml
Type: AuthenticationTypeEnum
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fa8-121">-DataSource</span><span class="sxs-lookup"><span data-stu-id="21fa8-121">-DataSource</span></span>
<span data-ttu-id="21fa8-122">Bağlanılacak sunucu adı.</span><span class="sxs-lookup"><span data-stu-id="21fa8-122">Server address\name to connect to.</span></span> 

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fa8-123">-TrustServerCertificate</span><span class="sxs-lookup"><span data-stu-id="21fa8-123">-TrustServerCertificate</span></span>
<span data-ttu-id="21fa8-124">Şifrelemenin gerçekleştiğini güvence altına almak için Boole değeri.</span><span class="sxs-lookup"><span data-stu-id="21fa8-124">Boolean indicating to guarantee that encryption takes place.</span></span>

```yaml
Type: Boolean
Parameter Sets: (All)
Aliases: 
Accepted values: SQL

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="21fa8-125">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="21fa8-125">-WhatIf</span></span>
<span data-ttu-id="21fa8-126">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="21fa8-126">Shows what would happen if the cmdlet runs.</span></span>
<span data-ttu-id="21fa8-127">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="21fa8-127">The cmdlet is not run.</span></span>

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





## <span data-ttu-id="21fa8-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="21fa8-128">INPUTS</span></span>

### <span data-ttu-id="21fa8-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="21fa8-129">None</span></span>


## <span data-ttu-id="21fa8-130">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="21fa8-130">OUTPUTS</span></span>

### <span data-ttu-id="21fa8-131">Microsoft. Azure. Management. DataMigration. modeller. ConnectionInfo</span><span class="sxs-lookup"><span data-stu-id="21fa8-131">Microsoft.Azure.Management.DataMigration.Models.ConnectionInfo</span></span>


## <span data-ttu-id="21fa8-132">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="21fa8-132">NOTES</span></span>

## <span data-ttu-id="21fa8-133">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="21fa8-133">RELATED LINKS</span></span>


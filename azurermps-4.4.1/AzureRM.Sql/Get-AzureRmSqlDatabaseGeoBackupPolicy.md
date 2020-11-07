---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
ms.assetid: 4F28BA63-23FC-4E35-A7FB-726E6FE94D26
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlDatabaseGeoBackupPolicy.md
ms.openlocfilehash: b8f7d04a709ebb14ed6a7a76cffab556c13d26ed
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764761"
---
# <span data-ttu-id="696c2-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="696c2-101">Get-AzureRmSqlDatabaseGeoBackupPolicy</span></span>

## <span data-ttu-id="696c2-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="696c2-102">SYNOPSIS</span></span>
<span data-ttu-id="696c2-103">Bir veritabanı coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="696c2-103">Gets a database geo backup policy.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="696c2-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="696c2-104">SYNTAX</span></span>

```
Get-AzureRmSqlDatabaseGeoBackupPolicy [-ServerName] <String> [-DatabaseName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="696c2-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="696c2-105">DESCRIPTION</span></span>
<span data-ttu-id="696c2-106">**Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet 'i, bu veritabanına kaydedilen coğrafi yedekleme ilkesini alır.</span><span class="sxs-lookup"><span data-stu-id="696c2-106">The **Get-AzureRmSqlDatabaseGeoBackupPolicy** cmdlet gets the geo backup policy registered to this database.</span></span>
<span data-ttu-id="696c2-107">Bu, yedek depolama ilkesini tanımlamak için kullanılan bir Azure yedekleme kaynağı.</span><span class="sxs-lookup"><span data-stu-id="696c2-107">This is an Azure Backup resource that is used to define backup storage policy.</span></span>

## <span data-ttu-id="696c2-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="696c2-108">EXAMPLES</span></span>

## <span data-ttu-id="696c2-109">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="696c2-109">PARAMETERS</span></span>

### <span data-ttu-id="696c2-110">-DatabaseName</span><span class="sxs-lookup"><span data-stu-id="696c2-110">-DatabaseName</span></span>
<span data-ttu-id="696c2-111">Bu cmdlet 'in coğrafi yedekleme ilkesini aldığı veritabanının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="696c2-111">Specifies the name of the database for which this cmdlet gets the geo backup policy.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="696c2-112">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="696c2-112">-ResourceGroupName</span></span>
<span data-ttu-id="696c2-113">Bu veritabanını içeren sunucunun kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="696c2-113">Specifies the name of the resource group of the server that contains this database.</span></span>

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

### <span data-ttu-id="696c2-114">-ServerName</span><span class="sxs-lookup"><span data-stu-id="696c2-114">-ServerName</span></span>
<span data-ttu-id="696c2-115">Veritabanını barındıran sunucunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="696c2-115">Specifies the name of the server that hosts the database.</span></span>

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

### <span data-ttu-id="696c2-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="696c2-116">-DefaultProfile</span></span>
<span data-ttu-id="696c2-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="696c2-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="696c2-118">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="696c2-118">CommonParameters</span></span>
<span data-ttu-id="696c2-119">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="696c2-119">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="696c2-120">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="696c2-120">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="696c2-121">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="696c2-121">INPUTS</span></span>

## <span data-ttu-id="696c2-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="696c2-122">OUTPUTS</span></span>

## <span data-ttu-id="696c2-123">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="696c2-123">NOTES</span></span>

## <span data-ttu-id="696c2-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="696c2-124">RELATED LINKS</span></span>

[<span data-ttu-id="696c2-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span><span class="sxs-lookup"><span data-stu-id="696c2-125">Set-AzureRmSqlDatabaseGeoBackupPolicy</span></span>](./Set-AzureRmSqlDatabaseGeoBackupPolicy.md)

[<span data-ttu-id="696c2-126">SQL veritabanı belgeleri</span><span class="sxs-lookup"><span data-stu-id="696c2-126">SQL Database Documentation</span></span>](https://docs.microsoft.com/azure/sql-database/)

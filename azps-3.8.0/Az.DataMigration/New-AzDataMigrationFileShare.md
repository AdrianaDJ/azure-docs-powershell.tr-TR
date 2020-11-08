---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: c0b88b60127162d895eeb642269240b699836d4f
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94096394"
---
# <span data-ttu-id="a3734-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a3734-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="a3734-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a3734-102">SYNOPSIS</span></span>
<span data-ttu-id="a3734-103">Kaynak veritabanı yedeklemelerini alacak yerel ağ paylaşımını belirten Azure veritabanı geçiş hizmeti için FileShare nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3734-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="a3734-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a3734-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a3734-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a3734-105">DESCRIPTION</span></span>
<span data-ttu-id="a3734-106">New-AzDataMigrationFileShare cmdlet 'i, Azure veritabanı geçiş hizmetinin kaynak veritabanı yedeklemelerini yapabileceği yerel ağ paylaşımını belirten FileShare nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a3734-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="a3734-107">Kaynak SQL Server örneğini çalıştıran hizmet hesabı bu ağ paylaşımında yazma ayrıcalıklarına sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a3734-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="a3734-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a3734-108">EXAMPLES</span></span>

### <span data-ttu-id="a3734-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a3734-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="a3734-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a3734-110">PARAMETERS</span></span>

### <span data-ttu-id="a3734-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="a3734-111">-Credential</span></span>
<span data-ttu-id="a3734-112">Dosya paylaşımına erişim için kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a3734-112">Credentials to access the file share.</span></span>

```yaml
Type: System.Management.Automation.PSCredential
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3734-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a3734-113">-DefaultProfile</span></span>
<span data-ttu-id="a3734-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a3734-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a3734-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="a3734-115">-Path</span></span>
<span data-ttu-id="a3734-116">Dosya paylaşım yolu.</span><span class="sxs-lookup"><span data-stu-id="a3734-116">File share path.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="a3734-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a3734-117">CommonParameters</span></span>
<span data-ttu-id="a3734-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a3734-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a3734-119">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a3734-119">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a3734-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a3734-120">INPUTS</span></span>

### <span data-ttu-id="a3734-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a3734-121">None</span></span>

## <span data-ttu-id="a3734-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a3734-122">OUTPUTS</span></span>

### <span data-ttu-id="a3734-123">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="a3734-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a3734-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a3734-124">NOTES</span></span>

## <span data-ttu-id="a3734-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a3734-125">RELATED LINKS</span></span>

---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataMigration.dll-Help.xml
Module Name: Az.DataMigration
online version: https://docs.microsoft.com/en-us/powershell/module/az.datamigration/New-AzDataMigrationFileShare
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataMigration/DataMigration/help/New-AzDataMigrationFileShare.md
ms.openlocfilehash: cc09f7ac0a5f4378c65700cd9681118200d629ed
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752252"
---
# <span data-ttu-id="a43a7-101">New-AzDataMigrationFileShare</span><span class="sxs-lookup"><span data-stu-id="a43a7-101">New-AzDataMigrationFileShare</span></span>

## <span data-ttu-id="a43a7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a43a7-102">SYNOPSIS</span></span>
<span data-ttu-id="a43a7-103">Kaynak veritabanı yedeklemelerini alacak yerel ağ paylaşımını belirten Azure veritabanı geçiş hizmeti için FileShare nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a43a7-103">Creates the FileShare object for the Azure Database Migration Service, which specifies the local network share to take the source database backups to.</span></span>

## <span data-ttu-id="a43a7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a43a7-104">SYNTAX</span></span>

```
New-AzDataMigrationFileShare -Path <String> -Credential <PSCredential>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a43a7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a43a7-105">DESCRIPTION</span></span>
<span data-ttu-id="a43a7-106">New-AzDataMigrationFileShare cmdlet 'i, Azure veritabanı geçiş hizmetinin kaynak veritabanı yedeklemelerini yapabileceği yerel ağ paylaşımını belirten FileShare nesnesini oluşturur.</span><span class="sxs-lookup"><span data-stu-id="a43a7-106">The New-AzDataMigrationFileShare cmdlet creates the FileShare object that specifies the local network share that Azure Database Migration Service can take source database backups to.</span></span> <span data-ttu-id="a43a7-107">Kaynak SQL Server örneğini çalıştıran hizmet hesabı bu ağ paylaşımında yazma ayrıcalıklarına sahip olmalıdır.</span><span class="sxs-lookup"><span data-stu-id="a43a7-107">The service account running source SQL Server instance must have write privileges on this network share.</span></span>

## <span data-ttu-id="a43a7-108">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a43a7-108">EXAMPLES</span></span>

### <span data-ttu-id="a43a7-109">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="a43a7-109">Example 1</span></span>
```
PS C:\> New-AzDmsFileShare -Path $fileSharePath -Credential $fileShareCred

UserName    Password     Path
--------    --------     ----
domain\user testadmin123 \\fileshare\folder1
```

## <span data-ttu-id="a43a7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a43a7-110">PARAMETERS</span></span>

### <span data-ttu-id="a43a7-111">-Credential</span><span class="sxs-lookup"><span data-stu-id="a43a7-111">-Credential</span></span>
<span data-ttu-id="a43a7-112">Dosya paylaşımına erişim için kimlik bilgileri.</span><span class="sxs-lookup"><span data-stu-id="a43a7-112">Credentials to access the file share.</span></span>

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

### <span data-ttu-id="a43a7-113">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a43a7-113">-DefaultProfile</span></span>
<span data-ttu-id="a43a7-114">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a43a7-114">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="a43a7-115">-Yol</span><span class="sxs-lookup"><span data-stu-id="a43a7-115">-Path</span></span>
<span data-ttu-id="a43a7-116">Dosya paylaşım yolu.</span><span class="sxs-lookup"><span data-stu-id="a43a7-116">File share path.</span></span>

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

### <span data-ttu-id="a43a7-117">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a43a7-117">CommonParameters</span></span>
<span data-ttu-id="a43a7-118">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a43a7-118">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a43a7-119">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a43a7-119">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a43a7-120">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a43a7-120">INPUTS</span></span>

### <span data-ttu-id="a43a7-121">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="a43a7-121">None</span></span>

## <span data-ttu-id="a43a7-122">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a43a7-122">OUTPUTS</span></span>

### <span data-ttu-id="a43a7-123">Microsoft. Azure. Management. DataMigration. modeller. Migratesqlserversqldbdatabaseınput</span><span class="sxs-lookup"><span data-stu-id="a43a7-123">Microsoft.Azure.Management.DataMigration.Models.MigrateSqlServerSqlDbDatabaseInput</span></span>

## <span data-ttu-id="a43a7-124">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a43a7-124">NOTES</span></span>

## <span data-ttu-id="a43a7-125">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a43a7-125">RELATED LINKS</span></span>
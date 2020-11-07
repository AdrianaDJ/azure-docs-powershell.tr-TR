---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/get-azsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 6ef3a84e84e001943cef1791c77f6c2a354da8ff
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93933857"
---
# <span data-ttu-id="82072-101">Get-AzSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="82072-101">Get-AzSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="82072-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="82072-102">SYNOPSIS</span></span>
<span data-ttu-id="82072-103">Bir eşitleme aracısıyla bağlantılı SQL Server veritabanları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="82072-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="82072-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="82072-104">SYNTAX</span></span>

```
Get-AzSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="82072-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="82072-105">DESCRIPTION</span></span>
<span data-ttu-id="82072-106">**Get-AzSqlSyncAgentLinkedDatabases** cmdlet 'i bir eşitleme ARACıSıYLA bağlantılı SQL Server veritabanları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="82072-106">The **Get-AzSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="82072-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="82072-107">EXAMPLES</span></span>

### <span data-ttu-id="82072-108">Örnek 1: Azure SQL eşitleme aracısının bağlantılı SQL Server veritabanlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="82072-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="82072-109">Bu komut, bir Azure SQL eşitleme Aracısı tarafından bağlantılı olan bağlantılı SQL Server veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="82072-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="82072-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="82072-110">PARAMETERS</span></span>

### <span data-ttu-id="82072-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="82072-111">-DefaultProfile</span></span>
<span data-ttu-id="82072-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="82072-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="82072-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="82072-113">-ResourceGroupName</span></span>
<span data-ttu-id="82072-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="82072-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="82072-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="82072-115">-ServerName</span></span>
<span data-ttu-id="82072-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="82072-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="82072-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="82072-117">-SyncAgentName</span></span>
<span data-ttu-id="82072-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="82072-118">The sync agent name.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: Name

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="82072-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="82072-119">CommonParameters</span></span>
<span data-ttu-id="82072-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="82072-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="82072-121">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="82072-121">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="82072-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="82072-122">INPUTS</span></span>

### <span data-ttu-id="82072-123">System. String</span><span class="sxs-lookup"><span data-stu-id="82072-123">System.String</span></span>

## <span data-ttu-id="82072-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="82072-124">OUTPUTS</span></span>

### <span data-ttu-id="82072-125">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentlinkeddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="82072-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="82072-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="82072-126">NOTES</span></span>

## <span data-ttu-id="82072-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="82072-127">RELATED LINKS</span></span>

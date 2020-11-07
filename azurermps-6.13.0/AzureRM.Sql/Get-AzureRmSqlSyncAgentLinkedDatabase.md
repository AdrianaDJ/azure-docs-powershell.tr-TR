---
external help file: Microsoft.Azure.Commands.Sql.dll-Help.xml
Module Name: AzureRM.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.sql/get-azurermsqlsyncagentlinkeddatabase
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Sql/Commands.Sql/help/Get-AzureRmSqlSyncAgentLinkedDatabase.md
ms.openlocfilehash: 11c444e92c6377e0a0df5aaa324ee162647784a1
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93764107"
---
# <span data-ttu-id="fc631-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span><span class="sxs-lookup"><span data-stu-id="fc631-101">Get-AzureRmSqlSyncAgentLinkedDatabase</span></span>

## <span data-ttu-id="fc631-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="fc631-102">SYNOPSIS</span></span>
<span data-ttu-id="fc631-103">Bir eşitleme aracısıyla bağlantılı SQL Server veritabanları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc631-103">Returns information about SQL Server databases linked by a sync agent.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="fc631-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="fc631-104">SYNTAX</span></span>

```
Get-AzureRmSqlSyncAgentLinkedDatabase [-ServerName] <String> [-SyncAgentName] <String>
 [-ResourceGroupName] <String> [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="fc631-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="fc631-105">DESCRIPTION</span></span>
<span data-ttu-id="fc631-106">**Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet 'i, bir eşitleme ARACıSıYLA bağlantılı SQL Server veritabanları hakkında bilgi döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc631-106">The **Get-AzureRmSqlSyncAgentLinkedDatabases** cmdlet returns information about SQL Server databases linked by a sync agent.</span></span>

## <span data-ttu-id="fc631-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="fc631-107">EXAMPLES</span></span>

### <span data-ttu-id="fc631-108">Örnek 1: Azure SQL eşitleme aracısının bağlantılı SQL Server veritabanlarını edinin.</span><span class="sxs-lookup"><span data-stu-id="fc631-108">Example 1: Get the linked SQL Server databases for an Azure SQL sync agent.</span></span>
```
PS C:\> Get-AzureRmSqlSyncAgentLinkedDatabases -ResourceGroupName "ResourceGroup01" -ServerName "Server01" -SyncAgentName "SyncAgent01" | Format-List
SeverName                 : sever01
DatabaseId                : databaseId
DatabaseName              : database01
DatabaseType              : SQLServerDatabase
Description               : 
UserName                  : myAccount
```

<span data-ttu-id="fc631-109">Bu komut, bir Azure SQL eşitleme Aracısı tarafından bağlantılı olan bağlantılı SQL Server veritabanlarını döndürür.</span><span class="sxs-lookup"><span data-stu-id="fc631-109">This command returns the linked SQL Server databases linked by an Azure SQL sync agent.</span></span>

## <span data-ttu-id="fc631-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="fc631-110">PARAMETERS</span></span>

### <span data-ttu-id="fc631-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="fc631-111">-DefaultProfile</span></span>
<span data-ttu-id="fc631-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik</span><span class="sxs-lookup"><span data-stu-id="fc631-112">The credentials, account, tenant, and subscription used for communication with azure</span></span>

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

### <span data-ttu-id="fc631-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="fc631-113">-ResourceGroupName</span></span>
<span data-ttu-id="fc631-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="fc631-114">The name of the resource group.</span></span>

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

### <span data-ttu-id="fc631-115">-ServerName</span><span class="sxs-lookup"><span data-stu-id="fc631-115">-ServerName</span></span>
<span data-ttu-id="fc631-116">Eşitleme aracısının bulunduğu Azure SQL Server 'ın adı.</span><span class="sxs-lookup"><span data-stu-id="fc631-116">The name of the Azure SQL Server the sync agent is in.</span></span>

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

### <span data-ttu-id="fc631-117">-SyncAgentName</span><span class="sxs-lookup"><span data-stu-id="fc631-117">-SyncAgentName</span></span>
<span data-ttu-id="fc631-118">Eşitleme aracısının adı.</span><span class="sxs-lookup"><span data-stu-id="fc631-118">The sync agent name.</span></span>

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

### <span data-ttu-id="fc631-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="fc631-119">CommonParameters</span></span>
<span data-ttu-id="fc631-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="fc631-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="fc631-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="fc631-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="fc631-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="fc631-122">INPUTS</span></span>

### <span data-ttu-id="fc631-123">System. String</span><span class="sxs-lookup"><span data-stu-id="fc631-123">System.String</span></span>

## <span data-ttu-id="fc631-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="fc631-124">OUTPUTS</span></span>

### <span data-ttu-id="fc631-125">Microsoft. Azure. Commands. Sql. DataSync. model. azures, Syncagentlinkeddatabasemodel</span><span class="sxs-lookup"><span data-stu-id="fc631-125">Microsoft.Azure.Commands.Sql.DataSync.Model.AzureSqlSyncAgentLinkedDatabaseModel</span></span>

## <span data-ttu-id="fc631-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="fc631-126">NOTES</span></span>

## <span data-ttu-id="fc631-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="fc631-127">RELATED LINKS</span></span>

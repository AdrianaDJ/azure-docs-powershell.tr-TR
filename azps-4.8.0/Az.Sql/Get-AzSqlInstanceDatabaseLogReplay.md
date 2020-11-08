---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Sql.dll-Help.xml
Module Name: Az.Sql
online version: https://docs.microsoft.com/en-us/powershell/module/az.sql/Get-AzSqlInstanceDatabaseLogReplay
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Sql/Sql/help/Get-AzSqlInstanceDatabaseLogReplay.md
ms.openlocfilehash: 7e37dcceb45370e4956fb59912a50a501fe271c1
ms.sourcegitcommit: 1de2b6c3c99197958fa2101bc37680e7507f91ac
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/13/2020
ms.locfileid: "94268727"
---
# <span data-ttu-id="d8bb3-101">Get-AzSqlInstanceDatabaseLogReplay</span><span class="sxs-lookup"><span data-stu-id="d8bb3-101">Get-AzSqlInstanceDatabaseLogReplay</span></span>

## <span data-ttu-id="d8bb3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="d8bb3-102">SYNOPSIS</span></span>
<span data-ttu-id="d8bb3-103">Günlük yürütme hizmeti durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-103">Gets the Log Replay service status.</span></span>

## <span data-ttu-id="d8bb3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="d8bb3-104">SYNTAX</span></span>

```
Get-AzSqlInstanceDatabaseLogReplay [[-Name] <String>] [-InstanceName] <String> [-ResourceGroupName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="d8bb3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="d8bb3-105">DESCRIPTION</span></span>
<span data-ttu-id="d8bb3-106">**Get-Azsqlınstancedatabaselogreplay** cmdlet 'i, verilen veritabanında günlük yürütme hizmeti durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-106">The **Get-AzSqlInstanceDatabaseLogReplay** cmdlet gets the Log Replay service status on the given database.</span></span>

## <span data-ttu-id="d8bb3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="d8bb3-107">EXAMPLES</span></span>

### <span data-ttu-id="d8bb3-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="d8bb3-108">Example 1</span></span>
```powershell
PS C:\> Get-AzSqlInstanceDatabaseLogReplay -ResourceGroupName "ResourceGroup01" -InstanceName "ManagedInstance01" -Name "ManagedDatabaseName"
```

<span data-ttu-id="d8bb3-109">Bu komut, verilen veritabanında günlük yürütme hizmeti durumunu alır.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-109">This command will get log replay service status on the given database.</span></span>

## <span data-ttu-id="d8bb3-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="d8bb3-110">PARAMETERS</span></span>

### <span data-ttu-id="d8bb3-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="d8bb3-111">-DefaultProfile</span></span>
<span data-ttu-id="d8bb3-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="d8bb3-113">-InstanceName</span><span class="sxs-lookup"><span data-stu-id="d8bb3-113">-InstanceName</span></span>
<span data-ttu-id="d8bb3-114">Örneğin adı.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-114">The name of the instance.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ManagedInstanceName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8bb3-115">-Ad</span><span class="sxs-lookup"><span data-stu-id="d8bb3-115">-Name</span></span>
<span data-ttu-id="d8bb3-116">Alınacak örnek veritabanının adı.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-116">The name of the instance database to retrieve.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: InstanceDatabaseName

Required: False
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="d8bb3-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="d8bb3-117">-ResourceGroupName</span></span>
<span data-ttu-id="d8bb3-118">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-118">The name of the resource group.</span></span>

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

### <span data-ttu-id="d8bb3-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="d8bb3-119">CommonParameters</span></span>
<span data-ttu-id="d8bb3-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="d8bb3-121">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="d8bb3-121">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="d8bb3-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="d8bb3-122">INPUTS</span></span>

### <span data-ttu-id="d8bb3-123">System. String</span><span class="sxs-lookup"><span data-stu-id="d8bb3-123">System.String</span></span>

## <span data-ttu-id="d8bb3-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="d8bb3-124">OUTPUTS</span></span>

### <span data-ttu-id="d8bb3-125">Microsoft. Azure. Commands. Sql. ManagedDatabase. model. AzureSqlManagedDatabaseRestoreDetailsResultModel</span><span class="sxs-lookup"><span data-stu-id="d8bb3-125">Microsoft.Azure.Commands.Sql.ManagedDatabase.Model.AzureSqlManagedDatabaseRestoreDetailsResultModel</span></span>

## <span data-ttu-id="d8bb3-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="d8bb3-126">NOTES</span></span>

## <span data-ttu-id="d8bb3-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="d8bb3-127">RELATED LINKS</span></span>

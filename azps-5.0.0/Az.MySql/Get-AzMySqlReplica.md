---
external help file: ''
Module Name: Az.MySql
online version: https://docs.microsoft.com/en-us/powershell/module/az.mysql/get-azmysqlreplica
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/MySql/help/Get-AzMySqlReplica.md
ms.openlocfilehash: 80f9e645c1c906e8275d3e25fb2ab833befa9328
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94319858"
---
# <span data-ttu-id="0dd50-101">Get-AzMySqlReplica</span><span class="sxs-lookup"><span data-stu-id="0dd50-101">Get-AzMySqlReplica</span></span>

## <span data-ttu-id="0dd50-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="0dd50-102">SYNOPSIS</span></span>
<span data-ttu-id="0dd50-103">Verilen sunucunun tüm çoğaltmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0dd50-103">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0dd50-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="0dd50-104">SYNTAX</span></span>

```
Get-AzMySqlReplica -ResourceGroupName <String> -ServerName <String> [-SubscriptionId <String[]>]
 [-DefaultProfile <PSObject>] [<CommonParameters>]
```

## <span data-ttu-id="0dd50-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="0dd50-105">DESCRIPTION</span></span>
<span data-ttu-id="0dd50-106">Verilen sunucunun tüm çoğaltmalarını listeler.</span><span class="sxs-lookup"><span data-stu-id="0dd50-106">List all the replicas for a given server.</span></span>

## <span data-ttu-id="0dd50-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="0dd50-107">EXAMPLES</span></span>

### <span data-ttu-id="0dd50-108">Örnek 1: kaynak grubuna ve sunucu adına göre MySql sunucu çoğaltmasını alma</span><span class="sxs-lookup"><span data-stu-id="0dd50-108">Example 1: Get MySql server replica by resource group and server name</span></span>
```powershell
PS C:\> Get-AzMySqlReplica -ResourceGroupName PowershellMySqlTest -ServerName mysql-test

Name               Location AdministratorLogin Version StorageProfileStorageMb SkuName   SkuTier        SslEnforcement
----               -------- ------------------ ------- ----------------------- -------   -------        --------------
mysql-test-replica eastus   mysql_test         5.7     10240                   GP_Gen5_4 GeneralPurpose Disabled
```

<span data-ttu-id="0dd50-109">Bu cmdlet, kaynak grubu ve sunucu adına göre MySql sunucu çoğaltmasını alır.</span><span class="sxs-lookup"><span data-stu-id="0dd50-109">This cmdlet gets MySql server replica by resource group and server name.</span></span>

## <span data-ttu-id="0dd50-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="0dd50-110">PARAMETERS</span></span>

### <span data-ttu-id="0dd50-111">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="0dd50-111">-DefaultProfile</span></span>
<span data-ttu-id="0dd50-112">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="0dd50-112">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

```yaml
Type: System.Management.Automation.PSObject
Parameter Sets: (All)
Aliases: AzureRMContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd50-113">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="0dd50-113">-ResourceGroupName</span></span>
<span data-ttu-id="0dd50-114">Kaynak grubunun adı.</span><span class="sxs-lookup"><span data-stu-id="0dd50-114">The name of the resource group.</span></span>
<span data-ttu-id="0dd50-115">Ad büyük/küçük harfe duyarlıdır.</span><span class="sxs-lookup"><span data-stu-id="0dd50-115">The name is case insensitive.</span></span>

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

### <span data-ttu-id="0dd50-116">-ServerName</span><span class="sxs-lookup"><span data-stu-id="0dd50-116">-ServerName</span></span>
<span data-ttu-id="0dd50-117">Sunucunun adı.</span><span class="sxs-lookup"><span data-stu-id="0dd50-117">The name of the server.</span></span>

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

### <span data-ttu-id="0dd50-118">-SubscriptionID</span><span class="sxs-lookup"><span data-stu-id="0dd50-118">-SubscriptionId</span></span>
<span data-ttu-id="0dd50-119">Hedef aboneliğin KIMLIĞI.</span><span class="sxs-lookup"><span data-stu-id="0dd50-119">The ID of the target subscription.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: (Get-AzContext).Subscription.Id
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="0dd50-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="0dd50-120">CommonParameters</span></span>
<span data-ttu-id="0dd50-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="0dd50-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="0dd50-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="0dd50-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="0dd50-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="0dd50-123">INPUTS</span></span>

## <span data-ttu-id="0dd50-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="0dd50-124">OUTPUTS</span></span>

### <span data-ttu-id="0dd50-125">Microsoft. Azure. PowerShell. cmdlet. MySql. modeller. Api20171201. IServer</span><span class="sxs-lookup"><span data-stu-id="0dd50-125">Microsoft.Azure.PowerShell.Cmdlets.MySql.Models.Api20171201.IServer</span></span>

## <span data-ttu-id="0dd50-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="0dd50-126">NOTES</span></span>

<span data-ttu-id="0dd50-127">DIĞER adları</span><span class="sxs-lookup"><span data-stu-id="0dd50-127">ALIASES</span></span>

## <span data-ttu-id="0dd50-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="0dd50-128">RELATED LINKS</span></span>


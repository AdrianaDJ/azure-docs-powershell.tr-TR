---
external help file: Microsoft.Azure.PowerShell.Cmdlets.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Az.AnalysisServices
online version: https://docs.microsoft.com/en-us/powershell/module/az.analysisservices/sync-azanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/AnalysisServices/AnalysisServices/help/Sync-AzAnalysisServicesInstance.md
ms.openlocfilehash: 2c7162f5a93c112a3f67b308941b56b698792fa3
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753625"
---
# <span data-ttu-id="84fa7-101">Sync-AzAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="84fa7-101">Sync-AzAnalysisServicesInstance</span></span>

## <span data-ttu-id="84fa7-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="84fa7-102">SYNOPSIS</span></span>

<span data-ttu-id="84fa7-103">Belirtilen Analysis Services Server örneğindeki belirli bir veritabanını, geçerli olarak oturum açmış olan ortamdaki tüm sorgu ölçeği örneklerinin Add-AzAnalysisServicesAccount komutta belirtildiği gibi eşitler</span><span class="sxs-lookup"><span data-stu-id="84fa7-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="84fa7-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="84fa7-104">SYNTAX</span></span>

```
Sync-AzAnalysisServicesInstance [-Database] <String> [-Instance] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="84fa7-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="84fa7-105">DESCRIPTION</span></span>

<span data-ttu-id="84fa7-106">Sync-AzAnalysisServicesInstance cmdlet 'i, Analysis Services sunucusundaki belirtilen bir veritabanını Add-AzAnalysisServicesAccount komutunda belirtilen geçerli olarak oturum açmış ortamdaki tüm sorgu ölçeği örneklerine eşitler</span><span class="sxs-lookup"><span data-stu-id="84fa7-106">The Sync-AzAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzAnalysisServicesAccount command</span></span>

## <span data-ttu-id="84fa7-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="84fa7-107">EXAMPLES</span></span>

### <span data-ttu-id="84fa7-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="84fa7-108">Example 1</span></span>

```
PS C:\>Sync-AzAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="84fa7-109">Bu komut, Add-AzAnalysisServicesAccount komutunu kullanarak Kullanıcı bu ortamda oturum açmış olduğundan westus.asazure.windows.net ortamdaki ' contoso ' adlı sunucudaki SalesOrders adlı veritabanını eşitler.</span><span class="sxs-lookup"><span data-stu-id="84fa7-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this environment using Add-AzAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="84fa7-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="84fa7-110">PARAMETERS</span></span>

### <span data-ttu-id="84fa7-111">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="84fa7-111">-Database</span></span>

<span data-ttu-id="84fa7-112">Eşitlenecek veritabanının kimliği</span><span class="sxs-lookup"><span data-stu-id="84fa7-112">Identity of the database to be synchronized</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84fa7-113">-Örnek</span><span class="sxs-lookup"><span data-stu-id="84fa7-113">-Instance</span></span>

<span data-ttu-id="84fa7-114">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="84fa7-114">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="84fa7-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="84fa7-115">-PassThru</span></span>

<span data-ttu-id="84fa7-116">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="84fa7-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fa7-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="84fa7-117">-Confirm</span></span>
<span data-ttu-id="84fa7-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="84fa7-118">Prompts you for confirmation before running the cmdlet.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: cf

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fa7-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="84fa7-119">-WhatIf</span></span>
<span data-ttu-id="84fa7-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="84fa7-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="84fa7-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="84fa7-121">The cmdlet is not run.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: (All)
Aliases: wi

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="84fa7-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="84fa7-122">CommonParameters</span></span>
<span data-ttu-id="84fa7-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="84fa7-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="84fa7-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="84fa7-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="84fa7-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="84fa7-125">INPUTS</span></span>

### <span data-ttu-id="84fa7-126">System. String</span><span class="sxs-lookup"><span data-stu-id="84fa7-126">System.String</span></span>

## <span data-ttu-id="84fa7-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="84fa7-127">OUTPUTS</span></span>

### <span data-ttu-id="84fa7-128">Microsoft. Azure. Commands. AnalysisServices. Datadüzlemi. model. ScaleOutServerDatabaseSyncDetails</span><span class="sxs-lookup"><span data-stu-id="84fa7-128">Microsoft.Azure.Commands.AnalysisServices.Dataplane.Models.ScaleOutServerDatabaseSyncDetails</span></span>

## <span data-ttu-id="84fa7-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="84fa7-129">NOTES</span></span>

<span data-ttu-id="84fa7-130">Diğer ad: Sync-AzAsInstance</span><span class="sxs-lookup"><span data-stu-id="84fa7-130">Alias: Sync-AzAsInstance</span></span>

## <span data-ttu-id="84fa7-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="84fa7-131">RELATED LINKS</span></span>

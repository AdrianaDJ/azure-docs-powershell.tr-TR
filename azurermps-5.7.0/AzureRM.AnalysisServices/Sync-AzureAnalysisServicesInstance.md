---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.analysisservices/sync-azureanalysisservicesinstance
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: f3fb2377fd78db4b330afd39a8691f958597f07a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588221"
---
# <span data-ttu-id="7d9de-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="7d9de-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="7d9de-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7d9de-102">SYNOPSIS</span></span>

<span data-ttu-id="7d9de-103">Belirtilen Analysis Services Server örneğindeki belirli bir veritabanını, geçerli olarak oturum açmış olan ortamdaki tüm sorgu ölçeği örneklerinin Add-AzureAnalysisServicesAccount komutta belirtildiği gibi eşitler</span><span class="sxs-lookup"><span data-stu-id="7d9de-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="7d9de-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7d9de-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-Passthru]
```

## <span data-ttu-id="7d9de-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7d9de-105">DESCRIPTION</span></span>

<span data-ttu-id="7d9de-106">Sync-AzureAnalysisServicesInstance cmdlet 'i, Analysis Services sunucusundaki belirtilen bir veritabanını Add-AzureAnalysisServicesAccount komutunda belirtilen geçerli olarak oturum açmış ortamdaki tüm sorgu ölçeği örneklerine eşitler</span><span class="sxs-lookup"><span data-stu-id="7d9de-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="7d9de-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7d9de-107">EXAMPLES</span></span>

### <span data-ttu-id="7d9de-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="7d9de-108">Example 1</span></span>

```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="7d9de-109">Bu komut, Add-AzureAnalysisServicesAccount komutu kullanarak kullanıcının bu enviroment oturum açtığı sağlanmış westus.asazure.windows.net ortamdaki ' contoso ' adlı sunucudaki SalesOrders adlı veritabanını eşitler.</span><span class="sxs-lookup"><span data-stu-id="7d9de-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="7d9de-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7d9de-110">PARAMETERS</span></span>

### <span data-ttu-id="7d9de-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="7d9de-111">-Instance</span></span>

<span data-ttu-id="7d9de-112">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="7d9de-112">Name of the Analysis Services server instance to restart</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9de-113">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="7d9de-113">-Database</span></span>

<span data-ttu-id="7d9de-114">Eşitlenecek veritabanının kimliği</span><span class="sxs-lookup"><span data-stu-id="7d9de-114">Identity of the database to be synchronized</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 
Required: True
Position: 0
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="7d9de-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="7d9de-115">-PassThru</span></span>

<span data-ttu-id="7d9de-116">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="7d9de-116">Specifying this will return true if the command was successful.</span></span>

```yaml
Type: Switch
Parameter Sets: (All)
Aliases: 
Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

## <span data-ttu-id="7d9de-117">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7d9de-117">INPUTS</span></span>

### <span data-ttu-id="7d9de-118">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="7d9de-118">None</span></span>
<span data-ttu-id="7d9de-119">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="7d9de-119">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="7d9de-120">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7d9de-120">OUTPUTS</span></span>

### <span data-ttu-id="7d9de-121">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="7d9de-121">System.Boolean</span></span>

## <span data-ttu-id="7d9de-122">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7d9de-122">NOTES</span></span>

<span data-ttu-id="7d9de-123">Diğer ad: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="7d9de-123">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="7d9de-124">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7d9de-124">RELATED LINKS</span></span>

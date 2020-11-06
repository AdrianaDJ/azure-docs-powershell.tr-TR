---
external help file: Microsoft.Azure.Commands.AnalysisServices.Dataplane.dll-Help.xml
Module Name: Azure.AnalysisServices
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AnalysisServices/Commands.AnalysisServices.Dataplane/help/Sync-AzureAnalysisServicesInstance.md
ms.openlocfilehash: a75ae79722fed99ce96b0a082f4f56ace998354e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93588017"
---
# <span data-ttu-id="20da8-101">Sync-AzureAnalysisServicesInstance</span><span class="sxs-lookup"><span data-stu-id="20da8-101">Sync-AzureAnalysisServicesInstance</span></span>

## <span data-ttu-id="20da8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="20da8-102">SYNOPSIS</span></span>
<span data-ttu-id="20da8-103">Belirtilen Analysis Services Server örneğindeki belirli bir veritabanını, geçerli olarak oturum açmış olan ortamdaki tüm sorgu ölçeği örneklerinin Add-AzureAnalysisServicesAccount komutta belirtildiği gibi eşitler</span><span class="sxs-lookup"><span data-stu-id="20da8-103">Synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="20da8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="20da8-104">SYNTAX</span></span>

```
Sync-AzureAnalysisServicesInstance [-Instance] <String> [-Database] <String> [-PassThru] [-WhatIf] [-Confirm]
 [<CommonParameters>]
```

## <span data-ttu-id="20da8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="20da8-105">DESCRIPTION</span></span>
<span data-ttu-id="20da8-106">Sync-AzureAnalysisServicesInstance cmdlet 'i, Analysis Services sunucusundaki belirtilen bir veritabanını Add-AzureAnalysisServicesAccount komutunda belirtilen geçerli olarak oturum açmış ortamdaki tüm sorgu ölçeği örneklerine eşitler</span><span class="sxs-lookup"><span data-stu-id="20da8-106">The Sync-AzureAnalysisServicesInstance cmdlet synchronizes a specified database on the specified instance of Analysis Services server to all the query scaleout instances in the currently logged in Environment as specified in Add-AzureAnalysisServicesAccount command</span></span>

## <span data-ttu-id="20da8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="20da8-107">EXAMPLES</span></span>

### <span data-ttu-id="20da8-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="20da8-108">Example 1</span></span>
```
PS C:\>Sync-AzureAnalysisServicesInstance -Instance asazure://westus.asazure.windows.net/contoso -Database SalesOrders
```

<span data-ttu-id="20da8-109">Bu komut, Add-AzureAnalysisServicesAccount komutu kullanarak kullanıcının bu enviroment oturum açtığı sağlanmış westus.asazure.windows.net ortamdaki ' contoso ' adlı sunucudaki SalesOrders adlı veritabanını eşitler.</span><span class="sxs-lookup"><span data-stu-id="20da8-109">This command will synchronize the database named SalesOrders in the server named 'contoso' in the environment westus.asazure.windows.net provided the user has logged-in to this enviroment using Add-AzureAnalysisServicesAccount command.</span></span>

## <span data-ttu-id="20da8-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="20da8-110">PARAMETERS</span></span>

### <span data-ttu-id="20da8-111">-Örnek</span><span class="sxs-lookup"><span data-stu-id="20da8-111">-Instance</span></span>
<span data-ttu-id="20da8-112">Yeniden başlatılacak Analysis Services sunucusu örneğinin adı</span><span class="sxs-lookup"><span data-stu-id="20da8-112">Name of the Analysis Services server instance to restart</span></span>

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

### <span data-ttu-id="20da8-113">-Veritabanı</span><span class="sxs-lookup"><span data-stu-id="20da8-113">-Database</span></span>
<span data-ttu-id="20da8-114">Eşitlenecek veritabanının kimliği</span><span class="sxs-lookup"><span data-stu-id="20da8-114">Identity of the database to be synchronized</span></span>

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

### <span data-ttu-id="20da8-115">-Geçiş</span><span class="sxs-lookup"><span data-stu-id="20da8-115">-PassThru</span></span>
<span data-ttu-id="20da8-116">Komut başarılı olmuşsa, bunu belirtmek doğru döndürür.</span><span class="sxs-lookup"><span data-stu-id="20da8-116">Specifying this will return true if the command was successful.</span></span>

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

### <span data-ttu-id="20da8-117">-Onay</span><span class="sxs-lookup"><span data-stu-id="20da8-117">-Confirm</span></span>
<span data-ttu-id="20da8-118">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="20da8-118">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="20da8-119">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="20da8-119">-WhatIf</span></span>
<span data-ttu-id="20da8-120">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="20da8-120">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="20da8-121">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="20da8-121">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="20da8-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="20da8-122">CommonParameters</span></span>
<span data-ttu-id="20da8-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="20da8-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="20da8-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="20da8-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="20da8-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="20da8-125">INPUTS</span></span>

## <span data-ttu-id="20da8-126">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="20da8-126">OUTPUTS</span></span>

### <span data-ttu-id="20da8-127">System. Boolean</span><span class="sxs-lookup"><span data-stu-id="20da8-127">System.Boolean</span></span>

## <span data-ttu-id="20da8-128">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="20da8-128">NOTES</span></span>
<span data-ttu-id="20da8-129">Diğer ad: Sync-AzureAsInstance</span><span class="sxs-lookup"><span data-stu-id="20da8-129">Alias: Sync-AzureAsInstance</span></span>

## <span data-ttu-id="20da8-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="20da8-130">RELATED LINKS</span></span>


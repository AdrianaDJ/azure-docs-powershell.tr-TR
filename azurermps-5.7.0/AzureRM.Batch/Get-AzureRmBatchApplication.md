---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/azurerm.batch/get-azurermbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: e22d3c58072fbabd3f927f6b9065f22422492622
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93586816"
---
# <span data-ttu-id="dff2a-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff2a-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="dff2a-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="dff2a-102">SYNOPSIS</span></span>
<span data-ttu-id="dff2a-103">Belirtilen uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dff2a-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="dff2a-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="dff2a-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="dff2a-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="dff2a-105">DESCRIPTION</span></span>
<span data-ttu-id="dff2a-106">**Get-AzureRmBatchApplication** cmdlet 'ı bir Azure toplu hesabındaki bir uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="dff2a-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="dff2a-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="dff2a-107">EXAMPLES</span></span>

### <span data-ttu-id="dff2a-108">Örnek 1: uygulamaları bir toplu Iş hesabında görüntüleme</span><span class="sxs-lookup"><span data-stu-id="dff2a-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="dff2a-109">Bu komut, ContosoBatch hesabındaki tüm uygulamaları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="dff2a-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="dff2a-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="dff2a-110">PARAMETERS</span></span>

### <span data-ttu-id="dff2a-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="dff2a-111">-AccountName</span></span>
<span data-ttu-id="dff2a-112">Uygulamayı içeren toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dff2a-112">Specifies the name of the Batch account that contains the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff2a-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="dff2a-113">-ApplicationId</span></span>
<span data-ttu-id="dff2a-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="dff2a-114">Specifies the ID of the application.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff2a-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="dff2a-115">-DefaultProfile</span></span>
<span data-ttu-id="dff2a-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="dff2a-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="dff2a-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="dff2a-117">-ResourceGroupName</span></span>
<span data-ttu-id="dff2a-118">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="dff2a-118">Specifies the name of the resource group that contains the Batch account.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="dff2a-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="dff2a-119">CommonParameters</span></span>
<span data-ttu-id="dff2a-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="dff2a-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="dff2a-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="dff2a-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="dff2a-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="dff2a-122">INPUTS</span></span>

### <span data-ttu-id="dff2a-123">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="dff2a-123">None</span></span>
<span data-ttu-id="dff2a-124">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="dff2a-124">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="dff2a-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="dff2a-125">OUTPUTS</span></span>

### <span data-ttu-id="dff2a-126">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="dff2a-126">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="dff2a-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="dff2a-127">NOTES</span></span>

## <span data-ttu-id="dff2a-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="dff2a-128">RELATED LINKS</span></span>

[<span data-ttu-id="dff2a-129">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff2a-129">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff2a-130">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff2a-130">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="dff2a-131">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff2a-131">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff2a-132">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff2a-132">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="dff2a-133">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="dff2a-133">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="dff2a-134">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="dff2a-134">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



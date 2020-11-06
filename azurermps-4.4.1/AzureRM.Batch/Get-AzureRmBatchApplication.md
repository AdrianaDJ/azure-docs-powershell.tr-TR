---
external help file: Microsoft.Azure.Commands.Batch.dll-Help.xml
Module Name: AzureRM.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/AzureBatch/Commands.Batch/help/Get-AzureRmBatchApplication.md
ms.openlocfilehash: b8169b2f05b4272c92989768e672b30aee105f19
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93593584"
---
# <span data-ttu-id="a224e-101">Get-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a224e-101">Get-AzureRmBatchApplication</span></span>

## <span data-ttu-id="a224e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="a224e-102">SYNOPSIS</span></span>
<span data-ttu-id="a224e-103">Belirtilen uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a224e-103">Gets information about the specified application.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="a224e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="a224e-104">SYNTAX</span></span>

```
Get-AzureRmBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="a224e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="a224e-105">DESCRIPTION</span></span>
<span data-ttu-id="a224e-106">**Get-AzureRmBatchApplication** cmdlet 'ı bir Azure toplu hesabındaki bir uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="a224e-106">The **Get-AzureRmBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="a224e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="a224e-107">EXAMPLES</span></span>

### <span data-ttu-id="a224e-108">Örnek 1: uygulamaları bir toplu Iş hesabında görüntüleme</span><span class="sxs-lookup"><span data-stu-id="a224e-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzureRmBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="a224e-109">Bu komut, ContosoBatch hesabındaki tüm uygulamaları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="a224e-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="a224e-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="a224e-110">PARAMETERS</span></span>

### <span data-ttu-id="a224e-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="a224e-111">-AccountName</span></span>
<span data-ttu-id="a224e-112">Uygulamayı içeren toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a224e-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="a224e-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="a224e-113">-ApplicationId</span></span>
<span data-ttu-id="a224e-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="a224e-114">Specifies the ID of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="a224e-115">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="a224e-115">-ResourceGroupName</span></span>
<span data-ttu-id="a224e-116">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="a224e-116">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="a224e-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="a224e-117">-DefaultProfile</span></span>
<span data-ttu-id="a224e-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="a224e-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="a224e-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="a224e-119">CommonParameters</span></span>
<span data-ttu-id="a224e-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="a224e-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="a224e-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="a224e-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="a224e-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="a224e-122">INPUTS</span></span>

## <span data-ttu-id="a224e-123">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="a224e-123">OUTPUTS</span></span>

### <span data-ttu-id="a224e-124">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="a224e-124">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="a224e-125">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="a224e-125">NOTES</span></span>

## <span data-ttu-id="a224e-126">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="a224e-126">RELATED LINKS</span></span>

[<span data-ttu-id="a224e-127">Get-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a224e-127">Get-AzureRmBatchApplicationPackage</span></span>](./Get-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a224e-128">Yeni-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a224e-128">New-AzureRmBatchApplication</span></span>](./New-AzureRmBatchApplication.md)

[<span data-ttu-id="a224e-129">Yeni-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a224e-129">New-AzureRmBatchApplicationPackage</span></span>](./New-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a224e-130">Remove-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a224e-130">Remove-AzureRmBatchApplication</span></span>](./Remove-AzureRmBatchApplication.md)

[<span data-ttu-id="a224e-131">Remove-AzureRmBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="a224e-131">Remove-AzureRmBatchApplicationPackage</span></span>](./Remove-AzureRmBatchApplicationPackage.md)

[<span data-ttu-id="a224e-132">Set-AzureRmBatchApplication</span><span class="sxs-lookup"><span data-stu-id="a224e-132">Set-AzureRmBatchApplication</span></span>](./Set-AzureRmBatchApplication.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: CF8B8E94-3C6C-4D68-B55B-956393890946
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/get-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Get-AzBatchApplication.md
ms.openlocfilehash: fa08214e141d035e7c449e591f6a4820f758b48c
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753183"
---
# <span data-ttu-id="bac7b-101">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bac7b-101">Get-AzBatchApplication</span></span>

## <span data-ttu-id="bac7b-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="bac7b-102">SYNOPSIS</span></span>
<span data-ttu-id="bac7b-103">Belirtilen uygulama hakkında bilgi alır.</span><span class="sxs-lookup"><span data-stu-id="bac7b-103">Gets information about the specified application.</span></span>

## <span data-ttu-id="bac7b-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="bac7b-104">SYNTAX</span></span>

```
Get-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [[-ApplicationId] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="bac7b-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="bac7b-105">DESCRIPTION</span></span>
<span data-ttu-id="bac7b-106">**Get-AzBatchApplication** cmdlet 'ı bir Azure toplu hesabındaki bir uygulamayla ilgili bilgileri alır.</span><span class="sxs-lookup"><span data-stu-id="bac7b-106">The **Get-AzBatchApplication** cmdlet gets information about an application in an Azure Batch account.</span></span>

## <span data-ttu-id="bac7b-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="bac7b-107">EXAMPLES</span></span>

### <span data-ttu-id="bac7b-108">Örnek 1: uygulamaları bir toplu Iş hesabında görüntüleme</span><span class="sxs-lookup"><span data-stu-id="bac7b-108">Example 1: Display the applications in a Batch account</span></span>
```
PS C:\>Get-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup"
ApplicationId AllowUpdates DisplayName

------------- ------------ ----------------------------

litware       False        Litware Advanced Reticulator
```

<span data-ttu-id="bac7b-109">Bu komut, ContosoBatch hesabındaki tüm uygulamaları görüntüler.</span><span class="sxs-lookup"><span data-stu-id="bac7b-109">This command displays all applications in the ContosoBatch account.</span></span>

## <span data-ttu-id="bac7b-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="bac7b-110">PARAMETERS</span></span>

### <span data-ttu-id="bac7b-111">-AccountName</span><span class="sxs-lookup"><span data-stu-id="bac7b-111">-AccountName</span></span>
<span data-ttu-id="bac7b-112">Uygulamayı içeren toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac7b-112">Specifies the name of the Batch account that contains the application.</span></span>

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

### <span data-ttu-id="bac7b-113">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="bac7b-113">-ApplicationId</span></span>
<span data-ttu-id="bac7b-114">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac7b-114">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="bac7b-115">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="bac7b-115">-DefaultProfile</span></span>
<span data-ttu-id="bac7b-116">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="bac7b-116">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="bac7b-117">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="bac7b-117">-ResourceGroupName</span></span>
<span data-ttu-id="bac7b-118">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="bac7b-118">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="bac7b-119">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="bac7b-119">CommonParameters</span></span>
<span data-ttu-id="bac7b-120">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="bac7b-120">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="bac7b-121">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="bac7b-121">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="bac7b-122">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="bac7b-122">INPUTS</span></span>

### <span data-ttu-id="bac7b-123">System. String</span><span class="sxs-lookup"><span data-stu-id="bac7b-123">System.String</span></span>

## <span data-ttu-id="bac7b-124">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="bac7b-124">OUTPUTS</span></span>

### <span data-ttu-id="bac7b-125">Microsoft.Azure.Commands.Batch. Modeller. PSApplication</span><span class="sxs-lookup"><span data-stu-id="bac7b-125">Microsoft.Azure.Commands.Batch.Models.PSApplication</span></span>

## <span data-ttu-id="bac7b-126">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="bac7b-126">NOTES</span></span>

## <span data-ttu-id="bac7b-127">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="bac7b-127">RELATED LINKS</span></span>

[<span data-ttu-id="bac7b-128">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bac7b-128">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="bac7b-129">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bac7b-129">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="bac7b-130">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bac7b-130">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="bac7b-131">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bac7b-131">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="bac7b-132">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="bac7b-132">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="bac7b-133">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="bac7b-133">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



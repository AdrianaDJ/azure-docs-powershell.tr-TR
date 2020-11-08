---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: 2CED21D6-4BEF-423B-A04A-5B812CEB975D
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplication.md
ms.openlocfilehash: 65840269419ee0cdfe322c9c6906e8ac4b368d1b
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097913"
---
# <span data-ttu-id="b3ea1-101">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b3ea1-101">Remove-AzBatchApplication</span></span>

## <span data-ttu-id="b3ea1-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b3ea1-102">SYNOPSIS</span></span>
<span data-ttu-id="b3ea1-103">Bir uygulamayı toplu Iş hesabından siler.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-103">Deletes an application from a Batch account.</span></span>

## <span data-ttu-id="b3ea1-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b3ea1-104">SYNTAX</span></span>

```
Remove-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="b3ea1-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b3ea1-105">DESCRIPTION</span></span>
<span data-ttu-id="b3ea1-106">**Remove-AzBatchApplication** cmdlet 'ı bir Azure toplu hesabından uygulamayı siler.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-106">The **Remove-AzBatchApplication** cmdlet deletes an application from an Azure Batch account.</span></span>

## <span data-ttu-id="b3ea1-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b3ea1-107">EXAMPLES</span></span>

### <span data-ttu-id="b3ea1-108">Örnek 1: bir uygulamayı toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="b3ea1-108">Example 1: Delete an application from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware"
```

<span data-ttu-id="b3ea1-109">Bu komut, ContosoBatch hesabından Litwin uygulamasını siler.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-109">This command deletes the Litware application from the ContosoBatch account.</span></span>
<span data-ttu-id="b3ea1-110">Uygulama herhangi bir paket içeriyorsa komut başarısız olur.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-110">The command fails if the application contains any packages.</span></span>

## <span data-ttu-id="b3ea1-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b3ea1-111">PARAMETERS</span></span>

### <span data-ttu-id="b3ea1-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="b3ea1-112">-AccountName</span></span>
<span data-ttu-id="b3ea1-113">Bu cmdlet 'in uygulamayı kaldırdığı toplu hesabın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-113">Specifies the name of the Batch account from which this cmdlet removes an application.</span></span>

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

### <span data-ttu-id="b3ea1-114">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="b3ea1-114">-ApplicationName</span></span>
<span data-ttu-id="b3ea1-115">Uygulamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-115">Specifies the name of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ApplicationId

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b3ea1-116">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="b3ea1-116">-DefaultProfile</span></span>
<span data-ttu-id="b3ea1-117">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-117">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="b3ea1-118">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b3ea1-118">-ResourceGroupName</span></span>
<span data-ttu-id="b3ea1-119">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-119">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="b3ea1-120">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b3ea1-120">CommonParameters</span></span>
<span data-ttu-id="b3ea1-121">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-121">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b3ea1-122">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="b3ea1-122">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b3ea1-123">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b3ea1-123">INPUTS</span></span>

### <span data-ttu-id="b3ea1-124">System. String</span><span class="sxs-lookup"><span data-stu-id="b3ea1-124">System.String</span></span>

## <span data-ttu-id="b3ea1-125">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b3ea1-125">OUTPUTS</span></span>

### <span data-ttu-id="b3ea1-126">System. void</span><span class="sxs-lookup"><span data-stu-id="b3ea1-126">System.Void</span></span>

## <span data-ttu-id="b3ea1-127">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b3ea1-127">NOTES</span></span>

## <span data-ttu-id="b3ea1-128">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b3ea1-128">RELATED LINKS</span></span>

[<span data-ttu-id="b3ea1-129">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b3ea1-129">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="b3ea1-130">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b3ea1-130">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="b3ea1-131">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b3ea1-131">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="b3ea1-132">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b3ea1-132">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="b3ea1-133">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="b3ea1-133">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)

[<span data-ttu-id="b3ea1-134">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="b3ea1-134">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)


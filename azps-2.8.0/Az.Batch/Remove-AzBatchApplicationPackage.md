---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: FD2E3442-9CEA-4390-BE9C-772C7D6FD1E2
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/remove-azbatchapplicationpackage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Remove-AzBatchApplicationPackage.md
ms.openlocfilehash: f4b47bb2abab783e4a6995ce57512dbd579e25e4
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93753168"
---
# <span data-ttu-id="7c46e-101">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7c46e-101">Remove-AzBatchApplicationPackage</span></span>

## <span data-ttu-id="7c46e-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="7c46e-102">SYNOPSIS</span></span>
<span data-ttu-id="7c46e-103">Uygulama paketi kaydını ve ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="7c46e-103">Deletes an application package record and the binary file.</span></span>

## <span data-ttu-id="7c46e-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="7c46e-104">SYNTAX</span></span>

```
Remove-AzBatchApplicationPackage [-AccountName] <String> [-ResourceGroupName] <String>
 [-ApplicationId] <String> [-ApplicationVersion] <String> [-DefaultProfile <IAzureContextContainer>]
 [<CommonParameters>]
```

## <span data-ttu-id="7c46e-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="7c46e-105">DESCRIPTION</span></span>
<span data-ttu-id="7c46e-106">**Remove-AzBatchApplicationPackage** cmdlet 'i, bir Azure toplu hesabındaki bir uygulama paketi kaydını ve ikili dosyayı siler.</span><span class="sxs-lookup"><span data-stu-id="7c46e-106">The **Remove-AzBatchApplicationPackage** cmdlet deletes an application package record and the binary file from an Azure Batch account.</span></span>

## <span data-ttu-id="7c46e-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="7c46e-107">EXAMPLES</span></span>

### <span data-ttu-id="7c46e-108">Örnek 1: bir uygulama paketini toplu hesaptan silme</span><span class="sxs-lookup"><span data-stu-id="7c46e-108">Example 1: Delete an application package from a Batch account</span></span>
```
PS C:\>Remove-AzBatchApplicationPackage -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationId "litware" -ApplicationVersion "1.0"
```

<span data-ttu-id="7c46e-109">Bu komut, ContosoBatchGroup hesabındaki Litwin uygulamasının 1,0 sürümünü siler.</span><span class="sxs-lookup"><span data-stu-id="7c46e-109">This command deletes version 1.0 of the Litware application from the ContosoBatchGroup account.</span></span>
<span data-ttu-id="7c46e-110">Komut hem paket kaydını hem de paket ikili dosyasını içeren blobu siler.</span><span class="sxs-lookup"><span data-stu-id="7c46e-110">The command deletes both the package record and the blob that contain the package binary file.</span></span>

## <span data-ttu-id="7c46e-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="7c46e-111">PARAMETERS</span></span>

### <span data-ttu-id="7c46e-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="7c46e-112">-AccountName</span></span>
<span data-ttu-id="7c46e-113">Bu cmdlet 'in uygulama paketini sildiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c46e-113">Specifies the name of the Batch account from which this cmdlet deletes an application package.</span></span>

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

### <span data-ttu-id="7c46e-114">-ApplicationId</span><span class="sxs-lookup"><span data-stu-id="7c46e-114">-ApplicationId</span></span>
<span data-ttu-id="7c46e-115">Uygulamanın KIMLIĞINI belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c46e-115">Specifies the ID of the application.</span></span>

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

### <span data-ttu-id="7c46e-116">-ApplicationVersion</span><span class="sxs-lookup"><span data-stu-id="7c46e-116">-ApplicationVersion</span></span>
<span data-ttu-id="7c46e-117">Uygulamanın sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c46e-117">Specifies the version of the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="7c46e-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="7c46e-118">-DefaultProfile</span></span>
<span data-ttu-id="7c46e-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="7c46e-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="7c46e-120">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="7c46e-120">-ResourceGroupName</span></span>
<span data-ttu-id="7c46e-121">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="7c46e-121">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="7c46e-122">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="7c46e-122">CommonParameters</span></span>
<span data-ttu-id="7c46e-123">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="7c46e-123">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="7c46e-124">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="7c46e-124">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="7c46e-125">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="7c46e-125">INPUTS</span></span>

### <span data-ttu-id="7c46e-126">System. String</span><span class="sxs-lookup"><span data-stu-id="7c46e-126">System.String</span></span>

## <span data-ttu-id="7c46e-127">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="7c46e-127">OUTPUTS</span></span>

### <span data-ttu-id="7c46e-128">System. void</span><span class="sxs-lookup"><span data-stu-id="7c46e-128">System.Void</span></span>

## <span data-ttu-id="7c46e-129">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="7c46e-129">NOTES</span></span>

## <span data-ttu-id="7c46e-130">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="7c46e-130">RELATED LINKS</span></span>

[<span data-ttu-id="7c46e-131">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7c46e-131">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="7c46e-132">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7c46e-132">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="7c46e-133">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7c46e-133">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="7c46e-134">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="7c46e-134">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="7c46e-135">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7c46e-135">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="7c46e-136">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="7c46e-136">Set-AzBatchApplication</span></span>](./Set-AzBatchApplication.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Batch.dll-Help.xml
Module Name: Az.Batch
ms.assetid: DCA1FD7A-54AF-48B1-A245-BFA9C43ACA9B
online version: https://docs.microsoft.com/en-us/powershell/module/az.batch/set-azbatchapplication
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Batch/Batch/help/Set-AzBatchApplication.md
ms.openlocfilehash: 6d6c72702d03b3b2174c21c786fb373374cea739
ms.sourcegitcommit: 6a91b4c545350d316d3cf8c62f384478e3f3ba24
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/21/2020
ms.locfileid: "94097905"
---
# <span data-ttu-id="15cc8-101">Set-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15cc8-101">Set-AzBatchApplication</span></span>

## <span data-ttu-id="15cc8-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="15cc8-102">SYNOPSIS</span></span>
<span data-ttu-id="15cc8-103">Belirtilen uygulama için güncelleştirme ayarları.</span><span class="sxs-lookup"><span data-stu-id="15cc8-103">Updates settings for the specified application.</span></span>

## <span data-ttu-id="15cc8-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="15cc8-104">SYNTAX</span></span>

```
Set-AzBatchApplication [-AccountName] <String> [-ResourceGroupName] <String> [-ApplicationName] <String>
 [[-DisplayName] <String>] [[-DefaultVersion] <String>] [[-AllowUpdates] <Boolean>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="15cc8-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="15cc8-105">DESCRIPTION</span></span>
<span data-ttu-id="15cc8-106">**Set-AzBatchApplication** cmdlet 'ı belirtilen Azure toplu iş uygulamasının ayarlarını değiştirir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-106">The **Set-AzBatchApplication** cmdlet modifies settings for the specified Azure Batch application.</span></span>

## <span data-ttu-id="15cc8-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="15cc8-107">EXAMPLES</span></span>

### <span data-ttu-id="15cc8-108">Örnek 1: toplu Iş hesabındaki bir uygulamayı güncelleştirme</span><span class="sxs-lookup"><span data-stu-id="15cc8-108">Example 1: Update an application in a Batch account</span></span>
```
PS C:\>Set-AzBatchApplication -AccountName "ContosoBatch" -ResourceGroupName "ContosoBatchGroup" -ApplicationName "Litware" -AllowUpdates $False
```

<span data-ttu-id="15cc8-109">Bu komut, ContosoBatch hesabındaki Litwin uygulamasının güncelleştirmelere izin verip vermediğini değiştirir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-109">This command changes whether the Litware application in the ContosoBatch account allows updates.</span></span>
<span data-ttu-id="15cc8-110">Komut, uygulamanın varsayılan sürümünü veya görünen adını değiştirmez.</span><span class="sxs-lookup"><span data-stu-id="15cc8-110">The command does not change the default version or display name of the application.</span></span>

## <span data-ttu-id="15cc8-111">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="15cc8-111">PARAMETERS</span></span>

### <span data-ttu-id="15cc8-112">-AccountName</span><span class="sxs-lookup"><span data-stu-id="15cc8-112">-AccountName</span></span>
<span data-ttu-id="15cc8-113">Bu cmdlet 'in bir uygulamayı değiştirdiği toplu Iş hesabının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-113">Specifies the name of the Batch account for which this cmdlet modifies an application.</span></span>

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

### <span data-ttu-id="15cc8-114">-AllowUpdates</span><span class="sxs-lookup"><span data-stu-id="15cc8-114">-AllowUpdates</span></span>
<span data-ttu-id="15cc8-115">Uygulamanın içindeki paketlerin aynı sürüm dizesini kullanarak yazılıp yazılmayacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-115">Specifies whether packages within the application can be overwritten using the same version string.</span></span>

```yaml
Type: System.Nullable`1[System.Boolean]
Parameter Sets: (All)
Aliases:

Required: False
Position: 5
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc8-116">-ApplicationName</span><span class="sxs-lookup"><span data-stu-id="15cc8-116">-ApplicationName</span></span>
<span data-ttu-id="15cc8-117">Uygulamanın adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-117">Specifies the name of the application.</span></span>

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

### <span data-ttu-id="15cc8-118">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="15cc8-118">-DefaultProfile</span></span>
<span data-ttu-id="15cc8-119">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="15cc8-119">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="15cc8-120">-DefaultVersion</span><span class="sxs-lookup"><span data-stu-id="15cc8-120">-DefaultVersion</span></span>
<span data-ttu-id="15cc8-121">Bir istemci uygulamayı istediğinde ancak bir sürüm belirtmezse hangi paketin kullanılacağını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-121">Specifies which package to use if a client requests the application but does not specify a version.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 4
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc8-122">-DisplayName</span><span class="sxs-lookup"><span data-stu-id="15cc8-122">-DisplayName</span></span>
<span data-ttu-id="15cc8-123">Uygulamanın görünen adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-123">Specifies the display name for the application.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: 3
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="15cc8-124">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="15cc8-124">-ResourceGroupName</span></span>
<span data-ttu-id="15cc8-125">Toplu Iş hesabını içeren kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="15cc8-125">Specifies the name of the resource group that contains the Batch account.</span></span>

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

### <span data-ttu-id="15cc8-126">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="15cc8-126">CommonParameters</span></span>
<span data-ttu-id="15cc8-127">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="15cc8-127">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="15cc8-128">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="15cc8-128">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="15cc8-129">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="15cc8-129">INPUTS</span></span>

### <span data-ttu-id="15cc8-130">System. String</span><span class="sxs-lookup"><span data-stu-id="15cc8-130">System.String</span></span>

### <span data-ttu-id="15cc8-131">System. Nullable ' 1 [[System. Boolean, mscorlib, Version = 4.0.0.0, Culture = neutral, PublicKeyToken = b77a5c561934e089]]</span><span class="sxs-lookup"><span data-stu-id="15cc8-131">System.Nullable\`1[[System.Boolean, mscorlib, Version=4.0.0.0, Culture=neutral, PublicKeyToken=b77a5c561934e089]]</span></span>

## <span data-ttu-id="15cc8-132">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="15cc8-132">OUTPUTS</span></span>

### <span data-ttu-id="15cc8-133">System. void</span><span class="sxs-lookup"><span data-stu-id="15cc8-133">System.Void</span></span>

## <span data-ttu-id="15cc8-134">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="15cc8-134">NOTES</span></span>

## <span data-ttu-id="15cc8-135">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="15cc8-135">RELATED LINKS</span></span>

[<span data-ttu-id="15cc8-136">Get-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15cc8-136">Get-AzBatchApplication</span></span>](./Get-AzBatchApplication.md)

[<span data-ttu-id="15cc8-137">Get-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15cc8-137">Get-AzBatchApplicationPackage</span></span>](./Get-AzBatchApplicationPackage.md)

[<span data-ttu-id="15cc8-138">New-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15cc8-138">New-AzBatchApplication</span></span>](./New-AzBatchApplication.md)

[<span data-ttu-id="15cc8-139">New-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15cc8-139">New-AzBatchApplicationPackage</span></span>](./New-AzBatchApplicationPackage.md)

[<span data-ttu-id="15cc8-140">Remove-AzBatchApplication</span><span class="sxs-lookup"><span data-stu-id="15cc8-140">Remove-AzBatchApplication</span></span>](./Remove-AzBatchApplication.md)

[<span data-ttu-id="15cc8-141">Remove-AzBatchApplicationPackage</span><span class="sxs-lookup"><span data-stu-id="15cc8-141">Remove-AzBatchApplicationPackage</span></span>](./Remove-AzBatchApplicationPackage.md)


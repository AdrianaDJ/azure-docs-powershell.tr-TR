---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: D5254218-8B3B-4DE2-9480-D65EE5483018
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmimage
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzVMImage.md
ms.openlocfilehash: 13871100efbe2fe62de769adcc40ee434e86eb21
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93752911"
---
# <span data-ttu-id="5a474-101">Get-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5a474-101">Get-AzVMImage</span></span>

## <span data-ttu-id="5a474-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5a474-102">SYNOPSIS</span></span>
<span data-ttu-id="5a474-103">Vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a474-103">Gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="5a474-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5a474-104">SYNTAX</span></span>

### <span data-ttu-id="5a474-105">ListVMImage</span><span class="sxs-lookup"><span data-stu-id="5a474-105">ListVMImage</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String>
 [-FilterExpression <String>] [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="5a474-106">Getvmımagedetail</span><span class="sxs-lookup"><span data-stu-id="5a474-106">GetVMImageDetail</span></span>
```
Get-AzVMImage -Location <String> -PublisherName <String> -Offer <String> -Skus <String> -Version <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="5a474-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="5a474-107">DESCRIPTION</span></span>
<span data-ttu-id="5a474-108">**Get-AzVMImage** cmdlet 'ı vmımage 'ın tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a474-108">The **Get-AzVMImage** cmdlet gets all the versions of a VMImage.</span></span>

## <span data-ttu-id="5a474-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5a474-109">EXAMPLES</span></span>

### <span data-ttu-id="5a474-110">Örnek 1: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="5a474-110">Example 1: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter"

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190104                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190115                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190204                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20190218                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="5a474-111">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a474-111">This command gets all the versions of VMImage that match the specified values.</span></span>

### <span data-ttu-id="5a474-112">Örnek 2: VMImage nesnesini alma</span><span class="sxs-lookup"><span data-stu-id="5a474-112">Example 2: Get VMImage object</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.20180315

Id               : /Subscriptions/xxxxxxxx-xxxx-xxxx-xxxx-xxxxxxxxxxxx/Providers/Microsoft.Compute/Locations/centralus/
                   Publishers/MicrosoftWindowsServer/ArtifactTypes/VMImage/Offers/windowsserver/Skus/2012-R2-Datacenter
                   /Versions/4.127.20180315
Location         : centralus
PublisherName    : MicrosoftWindowsServer
Offer            : windowsserver
Skus             : 2012-R2-Datacenter
Version          : 4.127.20180315
FilterExpression :
Name             : 4.127.20180315
OSDiskImage      : {
                     "operatingSystem": "Windows"
                   }
PurchasePlan     : null
DataDiskImages   : []
```

<span data-ttu-id="5a474-113">Bu komut, Vmımage 'ın belirtilen değerlerle eşleşen belirli bir sürümünü alır.</span><span class="sxs-lookup"><span data-stu-id="5a474-113">This command gets a specific version of VMImage that matches the specified values.</span></span>

### <span data-ttu-id="5a474-114">Örnek 3: Vmımage nesnelerini alma</span><span class="sxs-lookup"><span data-stu-id="5a474-114">Example 3: Get VMImage objects</span></span>
```
PS C:\> Get-AzVMImage -Location "Central US" -PublisherName "MicrosoftWindowsServer" -Offer "windowsserver" -Skus "2012-R2-Datacenter" -Version 4.127.2018*

Version        FilterExpression Skus               Offer         PublisherName          Location  Id
-------        ---------------- ----               -----         -------------          --------  --
4.127.20180315                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180510                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180815                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20180912                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181010                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
4.127.20181125                  2012-R2-Datacenter windowsserver MicrosoftWindowsServer centralus /Subscriptions/9e2...
```

<span data-ttu-id="5a474-115">Bu komut, tüm VMImage sürümü, sürüm üzerinde filtre uygulanan belirtilen değerlerle eşleşen tüm sürümlerini alır.</span><span class="sxs-lookup"><span data-stu-id="5a474-115">This command gets all the versions of VMImage that match the specified values with filtering over version.</span></span>

## <span data-ttu-id="5a474-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5a474-116">PARAMETERS</span></span>

### <span data-ttu-id="5a474-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="5a474-117">-DefaultProfile</span></span>
<span data-ttu-id="5a474-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="5a474-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="5a474-119">-FilterExpression</span><span class="sxs-lookup"><span data-stu-id="5a474-119">-FilterExpression</span></span>
<span data-ttu-id="5a474-120">Filtre ifadesi belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-120">Specifies a filter expression.</span></span>

```yaml
Type: System.String
Parameter Sets: ListVMImage
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5a474-121">-Konum</span><span class="sxs-lookup"><span data-stu-id="5a474-121">-Location</span></span>
<span data-ttu-id="5a474-122">Vmımage 'ın konumunu belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-122">Specifies the location of a VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a474-123">-Teklif</span><span class="sxs-lookup"><span data-stu-id="5a474-123">-Offer</span></span>
<span data-ttu-id="5a474-124">Vmımage teklifinin türünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-124">Specifies the type of VMImage offer.</span></span>
<span data-ttu-id="5a474-125">Resim teklifi edinmek için Get-AzVMImageOffer cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a474-125">To obtain an image offer, use the Get-AzVMImageOffer cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a474-126">-PublisherName</span><span class="sxs-lookup"><span data-stu-id="5a474-126">-PublisherName</span></span>
<span data-ttu-id="5a474-127">Vmımage 'ın yayımcısını belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-127">Specifies the publisher of a VMImage.</span></span>
<span data-ttu-id="5a474-128">Resim yayımcısı edinmek için Get-AzVMImagePublisher cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a474-128">To obtain an image publisher, use the Get-AzVMImagePublisher cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a474-129">-STB 'ler</span><span class="sxs-lookup"><span data-stu-id="5a474-129">-Skus</span></span>
<span data-ttu-id="5a474-130">Vmımage SKU 'SU belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-130">Specifies a VMImage SKU.</span></span>
<span data-ttu-id="5a474-131">SKU edinmek için Get-AzVMImageSku cmdlet 'ini kullanın.</span><span class="sxs-lookup"><span data-stu-id="5a474-131">To obtain an SKU, use the Get-AzVMImageSku cmdlet.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="5a474-132">-Version</span><span class="sxs-lookup"><span data-stu-id="5a474-132">-Version</span></span>
<span data-ttu-id="5a474-133">VMImage sürümünü belirtir.</span><span class="sxs-lookup"><span data-stu-id="5a474-133">Specifies the version of the VMImage.</span></span>

```yaml
Type: System.String
Parameter Sets: GetVMImageDetail
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: True
```

### <span data-ttu-id="5a474-134">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5a474-134">CommonParameters</span></span>
<span data-ttu-id="5a474-135">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5a474-135">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5a474-136">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="5a474-136">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5a474-137">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5a474-137">INPUTS</span></span>

### <span data-ttu-id="5a474-138">System. String</span><span class="sxs-lookup"><span data-stu-id="5a474-138">System.String</span></span>

## <span data-ttu-id="5a474-139">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5a474-139">OUTPUTS</span></span>

### <span data-ttu-id="5a474-140">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımage</span><span class="sxs-lookup"><span data-stu-id="5a474-140">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImage</span></span>

### <span data-ttu-id="5a474-141">Microsoft. Azure. Commands. COMPUTE. modeller. Psvirtualmachineımagedetail</span><span class="sxs-lookup"><span data-stu-id="5a474-141">Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineImageDetail</span></span>

## <span data-ttu-id="5a474-142">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5a474-142">NOTES</span></span>

## <span data-ttu-id="5a474-143">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5a474-143">RELATED LINKS</span></span>

[<span data-ttu-id="5a474-144">Get-Azvmımageteklifini</span><span class="sxs-lookup"><span data-stu-id="5a474-144">Get-AzVMImageOffer</span></span>](./Get-AzVMImageOffer.md)

[<span data-ttu-id="5a474-145">Get-Azvmımagepublisher</span><span class="sxs-lookup"><span data-stu-id="5a474-145">Get-AzVMImagePublisher</span></span>](./Get-AzVMImagePublisher.md)

[<span data-ttu-id="5a474-146">Get-AzVMImageSku</span><span class="sxs-lookup"><span data-stu-id="5a474-146">Get-AzVMImageSku</span></span>](./Get-AzVMImageSku.md)

[<span data-ttu-id="5a474-147">Save-AzVMImage</span><span class="sxs-lookup"><span data-stu-id="5a474-147">Save-AzVMImage</span></span>](./Save-AzVMImage.md)



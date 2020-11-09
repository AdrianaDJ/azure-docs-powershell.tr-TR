---
external help file: Microsoft.Azure.PowerShell.Cmdlets.DataBox.dll-Help.xml
Module Name: Az.DataBox
online version: https://docs.microsoft.com/en-us/powershell/module/az.databox/new-azdataboxjob
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/DataBox/DataBox/help/New-AzDataBoxJob.md
ms.openlocfilehash: 4402eaed4b76ce6e769141748b043598bdfd099a
ms.sourcegitcommit: b4a38bcb0501a9016a4998efd377aa75d3ef9ce8
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 10/27/2020
ms.locfileid: "94321265"
---
# <span data-ttu-id="6de57-101">New-AzDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6de57-101">New-AzDataBoxJob</span></span>

## <span data-ttu-id="6de57-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6de57-102">SYNOPSIS</span></span>
<span data-ttu-id="6de57-103">Belirtilen parametreleri kullanarak yeni bir veri kutusu işi oluşturur</span><span class="sxs-lookup"><span data-stu-id="6de57-103">Creates a new databox job using the specified parameters</span></span>

## <span data-ttu-id="6de57-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6de57-104">SYNTAX</span></span>

```
New-AzDataBoxJob -ResourceGroupName <String> -Name <String> [-DefaultProfile <IAzureContextContainer>]
 -Location <String> [-AddressType <AddressType>] [-CompanyName <String>] -StreetAddress1 <String>
 [-StreetAddress2 <String>] [-StreetAddress3 <String>] -PostalCode <String> -City <String>
 -StateOrProvinceCode <String> -CountryCode <String> -EmailId <String[]> -PhoneNumber <String>
 -ContactName <String> -StorageAccountResourceId <String[]> -DataBoxType <String>
 [-ExpectedDataSizeInTeraBytes <Int32>] [-WhatIf] [-Confirm] [<CommonParameters>]
```

## <span data-ttu-id="6de57-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6de57-105">DESCRIPTION</span></span>
<span data-ttu-id="6de57-106">**Yeni-Azveriboxjob** cmdlet 'i, işin oluşturulması için gereken ayrıntıları belirterek yeni bir veri kutusu işi oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="6de57-106">The **New-AzDataBoxJob** cmdlet is used to create a new databox job by specifying the details required for the creation of the job.</span></span>

## <span data-ttu-id="6de57-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6de57-107">EXAMPLES</span></span>

### <span data-ttu-id="6de57-108">Örnek 1</span><span class="sxs-lookup"><span data-stu-id="6de57-108">Example 1</span></span>
```powershell
PS C:\> $s1 = <Storage Account Resource Id>
PS C:\> New-AzDataBoxJob -Location 'WestUS' -StreetAddress1 '16 TOWNSEND ST' -PostalCode 94107 -City 'San Francisco' -StateOrProvinceCode 'CA' -CountryCode 'US' -EmailId 'abc@outlook.com' -PhoneNumber 1234567891 -ContactName 'John' -StorageAccount $s1 -DataBoxType DataBox -ResourceGroupName TestRg -Name OrderTest

jobResource.Name jobResource.Sku.Name jobResource.Status jobResource.StartTime jobResource.Location ResourceGroup
---------------- -------------------- ------------------ --------------------- -------------------- -------------
OrderTest       DataBox              DeviceOrdered      05-07-2019 05:25:30   westus               TestRg
```

<span data-ttu-id="6de57-109">Cmdlet, databox işini oluşturmak için gerekli tüm parametreleri ve isteğe bağlı bazı parametreleri alır.</span><span class="sxs-lookup"><span data-stu-id="6de57-109">The cmdlet takes all the required parameters and some optional parameters to create the databox job.</span></span>

## <span data-ttu-id="6de57-110">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6de57-110">PARAMETERS</span></span>

### <span data-ttu-id="6de57-111">-Adresstype</span><span class="sxs-lookup"><span data-stu-id="6de57-111">-AddressType</span></span>
<span data-ttu-id="6de57-112">Adres türü.</span><span class="sxs-lookup"><span data-stu-id="6de57-112">Type of Address.</span></span> <span data-ttu-id="6de57-113">Kullanılabilir değerler: AddressType. None (varsayılan), AddressType. konut, AddressType. Commercial</span><span class="sxs-lookup"><span data-stu-id="6de57-113">Available values : AddressType.None (default), AddressType.Residential, AddressType.Commercial</span></span>

```yaml
Type: Microsoft.Azure.Management.DataBox.Models.AddressType
Parameter Sets: (All)
Aliases:
Accepted values: None, Residential, Commercial

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-114">-Şehir</span><span class="sxs-lookup"><span data-stu-id="6de57-114">-City</span></span>
<span data-ttu-id="6de57-115">Şehrin adı.</span><span class="sxs-lookup"><span data-stu-id="6de57-115">Name of the City.</span></span> <span data-ttu-id="6de57-116">Ex: San Francisco</span><span class="sxs-lookup"><span data-stu-id="6de57-116">Ex : San Francisco</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-117">-ŞirketAdı</span><span class="sxs-lookup"><span data-stu-id="6de57-117">-CompanyName</span></span>
<span data-ttu-id="6de57-118">Şirketin adı</span><span class="sxs-lookup"><span data-stu-id="6de57-118">Name of the company</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-119">-Ilgilikişiadı</span><span class="sxs-lookup"><span data-stu-id="6de57-119">-ContactName</span></span>
<span data-ttu-id="6de57-120">Kişi adı</span><span class="sxs-lookup"><span data-stu-id="6de57-120">Contact Name</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-121">-CountryCode</span><span class="sxs-lookup"><span data-stu-id="6de57-121">-CountryCode</span></span>
<span data-ttu-id="6de57-122">Ülke kodu.</span><span class="sxs-lookup"><span data-stu-id="6de57-122">Country Code.</span></span> <span data-ttu-id="6de57-123">Ex: US</span><span class="sxs-lookup"><span data-stu-id="6de57-123">Ex: US</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-124">-DataBoxType</span><span class="sxs-lookup"><span data-stu-id="6de57-124">-DataBoxType</span></span>
<span data-ttu-id="6de57-125">Veri kutusunun SKU türü.</span><span class="sxs-lookup"><span data-stu-id="6de57-125">Sku type of Databox.</span></span>  <span data-ttu-id="6de57-126">Kullanılabilir değerler: DataBoxDisk, databox, DataBoxHeavy</span><span class="sxs-lookup"><span data-stu-id="6de57-126">Available values : DataBoxDisk, Databox, DataBoxHeavy</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:
Accepted values: DataBoxDisk, Databox, DataBoxHeavy

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-127">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6de57-127">-DefaultProfile</span></span>
<span data-ttu-id="6de57-128">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6de57-128">The credentials, account, tenant, and subscription used for communication with Azure.</span></span>

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

### <span data-ttu-id="6de57-129">-Emailıd</span><span class="sxs-lookup"><span data-stu-id="6de57-129">-EmailId</span></span>
<span data-ttu-id="6de57-130">Emailıds listesi sağlanabilir.</span><span class="sxs-lookup"><span data-stu-id="6de57-130">List of EmailIds can be provided.</span></span> <span data-ttu-id="6de57-131">En az bir zorunludur</span><span class="sxs-lookup"><span data-stu-id="6de57-131">Atleast one is mandatory</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-132">-ExpectedDataSizeInTeraBytes</span><span class="sxs-lookup"><span data-stu-id="6de57-132">-ExpectedDataSizeInTeraBytes</span></span>
<span data-ttu-id="6de57-133">DataBoxDisk sırası için, terabayttan beklenen verilerin belirtilmesi zorunludur.</span><span class="sxs-lookup"><span data-stu-id="6de57-133">For DataBoxDisk order, specifying the expected data in terabytes is mandatory.</span></span>

```yaml
Type: System.Int32
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-134">-Konum</span><span class="sxs-lookup"><span data-stu-id="6de57-134">-Location</span></span>
<span data-ttu-id="6de57-135">Aboneliğin konumu</span><span class="sxs-lookup"><span data-stu-id="6de57-135">Location of the subscription</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-136">-Ad</span><span class="sxs-lookup"><span data-stu-id="6de57-136">-Name</span></span>
<span data-ttu-id="6de57-137">Oluşturulacak veri kutusu işinin adı</span><span class="sxs-lookup"><span data-stu-id="6de57-137">Name of the databox job to be created</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-138">-PhoneNumber</span><span class="sxs-lookup"><span data-stu-id="6de57-138">-PhoneNumber</span></span>
<span data-ttu-id="6de57-139">Kişi numarası</span><span class="sxs-lookup"><span data-stu-id="6de57-139">Contact Number</span></span> 

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-140">-PostaKodu</span><span class="sxs-lookup"><span data-stu-id="6de57-140">-PostalCode</span></span>
<span data-ttu-id="6de57-141">Posta kodu</span><span class="sxs-lookup"><span data-stu-id="6de57-141">Postal Code</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-142">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6de57-142">-ResourceGroupName</span></span>
<span data-ttu-id="6de57-143">Veri kutusu işinin altında oluşturulması gereken kaynak grubu adı.</span><span class="sxs-lookup"><span data-stu-id="6de57-143">Resource Group Name under which the databox job has to be created.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-144">-StateOrProvinceCode</span><span class="sxs-lookup"><span data-stu-id="6de57-144">-StateOrProvinceCode</span></span>
<span data-ttu-id="6de57-145">Eyalet veya il kodunu girin.</span><span class="sxs-lookup"><span data-stu-id="6de57-145">Input the state or province code.</span></span> <span data-ttu-id="6de57-146">CA gibi-California; FL-Florida; NY-New York</span><span class="sxs-lookup"><span data-stu-id="6de57-146">Like CA - California; FL - Florida; NY - New York</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-147">-Storageaccountresourceıd</span><span class="sxs-lookup"><span data-stu-id="6de57-147">-StorageAccountResourceId</span></span>
<span data-ttu-id="6de57-148">Depolama hesaplarının kaynak kimliklerinin listesi.</span><span class="sxs-lookup"><span data-stu-id="6de57-148">List of Resource Ids of Storage Accounts.</span></span> <span data-ttu-id="6de57-149">En az bir zorunludur.</span><span class="sxs-lookup"><span data-stu-id="6de57-149">Atleast one is mandatory.</span></span>

```yaml
Type: System.String[]
Parameter Sets: (All)
Aliases: Id

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-150">-StreetAddress1</span><span class="sxs-lookup"><span data-stu-id="6de57-150">-StreetAddress1</span></span>
<span data-ttu-id="6de57-151">Sokak adresi</span><span class="sxs-lookup"><span data-stu-id="6de57-151">Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: True
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-152">-StreetAddress2</span><span class="sxs-lookup"><span data-stu-id="6de57-152">-StreetAddress2</span></span>
<span data-ttu-id="6de57-153">Ek sokak adresi</span><span class="sxs-lookup"><span data-stu-id="6de57-153">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-154">-StreetAddress3</span><span class="sxs-lookup"><span data-stu-id="6de57-154">-StreetAddress3</span></span>
<span data-ttu-id="6de57-155">Ek sokak adresi</span><span class="sxs-lookup"><span data-stu-id="6de57-155">Additional Street Address</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases:

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6de57-156">-Onay</span><span class="sxs-lookup"><span data-stu-id="6de57-156">-Confirm</span></span>
<span data-ttu-id="6de57-157">Cmdlet 'i çalıştırmadan önce onaylamanızı ister.</span><span class="sxs-lookup"><span data-stu-id="6de57-157">Prompts you for confirmation before running the cmdlet.</span></span>

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

### <span data-ttu-id="6de57-158">-WhatIf</span><span class="sxs-lookup"><span data-stu-id="6de57-158">-WhatIf</span></span>
<span data-ttu-id="6de57-159">Cmdlet çalışırsa ne olacağını gösterir.</span><span class="sxs-lookup"><span data-stu-id="6de57-159">Shows what would happen if the cmdlet runs.</span></span> <span data-ttu-id="6de57-160">Cmdlet çalışmaz.</span><span class="sxs-lookup"><span data-stu-id="6de57-160">The cmdlet is not run.</span></span>

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

### <span data-ttu-id="6de57-161">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6de57-161">CommonParameters</span></span>
<span data-ttu-id="6de57-162">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6de57-162">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6de57-163">Daha fazla bilgi için [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6de57-163">For more information, see [about_CommonParameters](http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6de57-164">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6de57-164">INPUTS</span></span>

### <span data-ttu-id="6de57-165">System. String []</span><span class="sxs-lookup"><span data-stu-id="6de57-165">System.String[]</span></span>

## <span data-ttu-id="6de57-166">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6de57-166">OUTPUTS</span></span>

### <span data-ttu-id="6de57-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span><span class="sxs-lookup"><span data-stu-id="6de57-167">Microsoft.Azure.PowerShell.Cmdlets.DataBox.Models.PSDataBoxJob</span></span>

## <span data-ttu-id="6de57-168">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6de57-168">NOTES</span></span>

## <span data-ttu-id="6de57-169">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6de57-169">RELATED LINKS</span></span>

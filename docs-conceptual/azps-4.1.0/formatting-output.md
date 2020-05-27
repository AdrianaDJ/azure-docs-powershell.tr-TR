---
title: Azure PowerShell cmdlet'inin çıkışını biçimlendirme
description: Azure PowerShell için cmdlet çıkışını biçimlendirme.
ms.devlang: powershell
ms.topic: conceptual
ms.date: 01/07/2019
ms.openlocfilehash: dbce06569ada169cdd93ae85d40e1554a7f7fdec
ms.sourcegitcommit: 10ec909100a70acec94d42f6084e7bf0342c6854
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 05/19/2020
ms.locfileid: "83630801"
---
# <a name="format-azure-powershell-cmdlet-output"></a><span data-ttu-id="944a1-103">Azure PowerShell cmdlet'inin çıkışını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="944a1-103">Format Azure PowerShell cmdlet output</span></span>

<span data-ttu-id="944a1-104">Varsayılan olarak tüm Azure PowerShell cmdlet'leri çıkışı kolay okunacak şekilde biçimlendirir.</span><span class="sxs-lookup"><span data-stu-id="944a1-104">By default each Azure PowerShell cmdlet formats output to be easy to read.</span></span> <span data-ttu-id="944a1-105">PowerShell, sizi aşağıdaki cmdlet'lerden birine yönlendirerek cmdlet çıkışını dönüştürmenize veya biçimlendirmenize olanak tanır:</span><span class="sxs-lookup"><span data-stu-id="944a1-105">PowerShell allows you to convert or format cmdlet output by piping to one of the following cmdlets:</span></span>

| <span data-ttu-id="944a1-106">Biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="944a1-106">Formatting</span></span>      | <span data-ttu-id="944a1-107">Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="944a1-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="944a1-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="944a1-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="944a1-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="944a1-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="944a1-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="944a1-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="944a1-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="944a1-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="944a1-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="944a1-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="944a1-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="944a1-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="944a1-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="944a1-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="944a1-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

<span data-ttu-id="944a1-116">Biçimlendirme PowerShell terminalinde görüntülemek için ve dönüştürme de diğer betikler veya programlar tarafından kullanılacak verileri oluşturmak için kullanılır.</span><span class="sxs-lookup"><span data-stu-id="944a1-116">Formatting is used for display in a PowerShell terminal, and conversion is used for generating data to be consumed by other scripts or programs.</span></span>

## <a name="table-output-format"></a><span data-ttu-id="944a1-117">Tablo çıkış biçimi</span><span class="sxs-lookup"><span data-stu-id="944a1-117">Table output format</span></span>

<span data-ttu-id="944a1-118">Varsayılan olarak, Azure PowerShell cmdlet'lerinin çıkışı tablo biçiminde olur.</span><span class="sxs-lookup"><span data-stu-id="944a1-118">By default, Azure PowerShell cmdlets output in the table format.</span></span> <span data-ttu-id="944a1-119">Bu biçim, istenen kaynağın tüm bilgilerini görüntülemez:</span><span class="sxs-lookup"><span data-stu-id="944a1-119">This format doesn't display all information of the requested resource:</span></span>

```powershell-interactive
Get-AzVM
```

```output
ResourceGroupName           Name Location          VmSize  OsType               NIC ProvisioningState Zone
-----------------           ---- --------          ------  ------               --- ----------------- ----
QueryExample      ExampleLinuxVM  westus2        Basic_A0   Linux examplelinuxvm916         Succeeded
QueryExample         RHELExample  westus2  Standard_D2_v3   Linux    rhelexample469         Succeeded
QueryExample        WinExampleVM  westus2 Standard_DS1_v2 Windows   winexamplevm268         Succeeded
```

<span data-ttu-id="944a1-120">`Format-Table` tarafından görüntülenen veri miktarı, PowerShell oturum pencerenizin genişliğinden etkilenebilir.</span><span class="sxs-lookup"><span data-stu-id="944a1-120">The amount of data displayed by `Format-Table` can be affected by the width of your PowerShell session window.</span></span> <span data-ttu-id="944a1-121">Çıkışı belirli özelliklerle sınırlamak ve bunları sıralamak için, özellik adları `Format-Table` cmdlet'ine bağımsız değişken olarak sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="944a1-121">To restrict the output to specific properties and order them, property names can be provided as arguments to `Format-Table`:</span></span>

```powershell-interactive
Get-AzVM -ResourceGroupName QueryExample | Format-Table Name,ResourceGroupName,Location
```

```output
Name           ResourceGroupName Location
----           ----------------- --------
ExampleLinuxVM QueryExample      westus2
RHELExample    QueryExample      westus2
WinExampleVM   QueryExample      westus2
```

## <a name="list-output-format"></a><span data-ttu-id="944a1-122">Liste çıkış biçimi</span><span class="sxs-lookup"><span data-stu-id="944a1-122">List output format</span></span>

<span data-ttu-id="944a1-123">Liste çıkış biçimi, özellik adlarını ve ardından değeri içeren iki sütun oluşturur.</span><span class="sxs-lookup"><span data-stu-id="944a1-123">List output format produces two columns, property names followed by the value.</span></span> <span data-ttu-id="944a1-124">Karmaşık nesnelerde, bunun yerine nesnenin türü görüntülenir.</span><span class="sxs-lookup"><span data-stu-id="944a1-124">For complex objects, the type of the object is displayed instead.</span></span>

```powershell-interactive
Get-AzVM | Format-List
```

<span data-ttu-id="944a1-125">Aşağıdaki çıkışta bazı alanlar kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="944a1-125">The following output has some fields removed.</span></span>

```output
ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId                     : ...
Name                     : ExampleLinuxVM
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
HardwareProfile          : Microsoft.Azure.Management.Compute.Models.HardwareProfile
InstanceView             :
NetworkProfile           : Microsoft.Azure.Management.Compute.Models.NetworkProfile
OSProfile                : Microsoft.Azure.Management.Compute.Models.OSProfile
...
StatusCode               : OK

ResourceGroupName        : QueryExample
Id                       : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/RHELExample
VmId                     : ...
Name                     : RHELExample
Type                     : Microsoft.Compute/virtualMachines
Location                 : westus2
...
```

<span data-ttu-id="944a1-126">Aynı `Format-Table` gibi, çıkışı sıralamak ve kısıtlamak için özellik adları sağlanabilir:</span><span class="sxs-lookup"><span data-stu-id="944a1-126">Like `Format-Table`, property names can be provided to order and restrict the output:</span></span>

```powershell-interactive
Get-AzVM | Format-List ResourceGroupName,Name,Location
```

```output
ResourceGroupName : QueryExample
Name              : ExampleLinuxVM
Location          : westus2

ResourceGroupName : QueryExample
Name              : RHELExample
Location          : westus2

ResourceGroupName : QueryExample
Name              : WinExampleVM
Location          : westus2
```

## <a name="wide-output-format"></a><span data-ttu-id="944a1-127">Geniş çıkış biçimi</span><span class="sxs-lookup"><span data-stu-id="944a1-127">Wide output format</span></span>

<span data-ttu-id="944a1-128">Geniş çıkış biçimi sorgu başına tek bir özellik adı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="944a1-128">Wide output format produces only one property name per query.</span></span> <span data-ttu-id="944a1-129">Hangi özelliğin görüntüleneceği, bir özelliği bağımsız değişken olarak sağlayarak denetlenebilir.</span><span class="sxs-lookup"><span data-stu-id="944a1-129">Which property is displayed can be controlled by giving a property as an argument.</span></span>

```powershell-interactive
Get-AzVM | Format-Wide
```

```output
ExampleLinuxVM                                  RHELExample
WinExampleVM
```

```powershell-interactive
Get-AzVM | Format-Wide ResourceGroupName
```

```output
QueryExample                                    QueryExample
QueryExample
```

## <a name="custom-output-format"></a><span data-ttu-id="944a1-130">Özel çıkış biçimi</span><span class="sxs-lookup"><span data-stu-id="944a1-130">Custom output format</span></span>

<span data-ttu-id="944a1-131">Özel nesneleri biçimlendirmek için `Custom-Format` çıkış türü tasarlanmıştır.</span><span class="sxs-lookup"><span data-stu-id="944a1-131">The `Custom-Format` output type is meant for formatting custom objects.</span></span> <span data-ttu-id="944a1-132">Hiçbir bağımsız değişken sağlanmadığında, `Format-List` cmdlet'i gibi davranır ama özel sınıfların özellik adlarını görüntüler.</span><span class="sxs-lookup"><span data-stu-id="944a1-132">Without any arguments, it behaves like `Format-List` but displays the property names of custom classes.</span></span>

```powershell-interactive
Get-AzVM | Format-Custom
```

<span data-ttu-id="944a1-133">Aşağıdaki çıkışta bazı alanlar kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="944a1-133">The following output has some fields removed.</span></span>

```output
ResourceGroupName : QueryExample
Id                : /subscriptions/.../resourceGroups/QueryExample/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM
VmId              : ...
Name              : ExampleLinuxVM
Type              : Microsoft.Compute/virtualMachines
Location          : westus2
Tags              : {}
HardwareProfile   : {VmSize}
NetworkProfile    : {NetworkInterfaces}
OSProfile         : {ComputerName, AdminUsername, LinuxConfiguration, Secrets,
AllowExtensionOperations}
ProvisioningState : Succeeded
StorageProfile    : {ImageReference, OsDisk, DataDisks}
...
```

<span data-ttu-id="944a1-134">`Custom-Format` cmdlet'ine özellik adları bağımsız değişken olarak verildiğinde, özel nesneler için değer olarak ayarlanan özellik/değer çiftleri görüntülenir:</span><span class="sxs-lookup"><span data-stu-id="944a1-134">Giving property names as arguments to `Custom-Format` displays the property/value pairs for custom objects set as values:</span></span>

```powershell-interactive
Get-AzVM | Format-Custom Name,ResourceGroupName,Location,OSProfile
```

<span data-ttu-id="944a1-135">Aşağıdaki çıkışta bazı alanlar kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="944a1-135">The following output has some fields removed.</span></span>

```output
class PSVirtualMachineList
{
  Name = ExampleLinuxVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = ExampleLinuxVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
      LinuxConfiguration =
        class LinuxConfiguration
        {
          DisablePasswordAuthentication = False
          Ssh =
          ProvisionVMAgent = True
        }
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}

...

class PSVirtualMachineList
{
  Name = WinExampleVM
  ResourceGroupName = QueryExample
  Location = westus2
  OSProfile =
    class OSProfile
    {
      ComputerName = WinExampleVM
      AdminUsername = ...
      AdminPassword =
      CustomData =
      WindowsConfiguration =
        class WindowsConfiguration
        {
          ProvisionVMAgent = True
          EnableAutomaticUpdates = True
          TimeZone =
          AdditionalUnattendContent =
          WinRM =
        }
      LinuxConfiguration =
      Secrets =
        [
        ]

      AllowExtensionOperations = True
    }
}
```

## <a name="conversion-to-other-data-formats"></a><span data-ttu-id="944a1-136">Diğer veri biçimlerine dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-136">Conversion to other data formats</span></span>

<span data-ttu-id="944a1-137">`ConvertTo-*` cmdlet ailesi, Azure PowerShell cmdlet'lerinin sonuçlarını makine tarafından okunabilir biçimlere dönüştürmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="944a1-137">The `ConvertTo-*` family of cmdlets allows for converting the results of Azure PowerShell cmdlets to machine-readable formats.</span></span> <span data-ttu-id="944a1-138">Azure PowerShell sonuçlarından yalnızca bazı özellikleri almak için, dönüştürmeyi yapmadan önce bir kanalda `Select-Object` komutunu kullanın.</span><span class="sxs-lookup"><span data-stu-id="944a1-138">To get only some properties from the Azure PowerShell results, use the `Select-Object` command in a pipe before performing the conversion.</span></span> <span data-ttu-id="944a1-139">Aşağıdaki örneklerde, her dönüştürmenin oluşturduğu farklı çıkış türleri gösterilir.</span><span class="sxs-lookup"><span data-stu-id="944a1-139">The following examples demonstrate the different kinds of output that each conversion produces.</span></span>

### <a name="conversion-to-csv"></a><span data-ttu-id="944a1-140">CSV'ye dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-140">Conversion to CSV</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-CSV
```

```output
#TYPE Microsoft.Azure.Commands.Compute.Models.PSVirtualMachineList
"ResourceGroupName","Id","VmId","Name","Type","Location","LicenseType","Tags","AvailabilitySetReference","DiagnosticsProfile","Extensions","HardwareProfile","InstanceView","NetworkProfile","OSProfile","Plan","ProvisioningState","StorageProfile","DisplayHint","Identity","Zones","FullyQualifiedDomainName","AdditionalCapabilities","RequestId","StatusCode"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM","...","ExampleLinuxVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample","...","RHELExample","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
"QUERYEXAMPLE","/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM","...","WinExampleVM","Microsoft.Compute/virtualMachines","westus2",,"System.Collections.Generic.Dictionary`2[System.String,System.String]",,,"System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]","Microsoft.Azure.Management.Compute.Models.HardwareProfile",,"Microsoft.Azure.Management.Compute.Models.NetworkProfile","Microsoft.Azure.Management.Compute.Models.OSProfile",,"Succeeded","Microsoft.Azure.Management.Compute.Models.StorageProfile","Compact",,"System.Collections.Generic.List`1[System.String]",,,"...","OK"
```

### <a name="conversion-to-json"></a><span data-ttu-id="944a1-141">JSON'ye dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-141">Conversion to JSON</span></span>

<span data-ttu-id="944a1-142">JSON çıkışı varsayılan olarak tüm özellikleri genişletmez.</span><span class="sxs-lookup"><span data-stu-id="944a1-142">JSON output doesn't expand all properties by default.</span></span> <span data-ttu-id="944a1-143">Genişletilen özelliklerin derinliğini değiştirmek için `-Depth` bağımsız değişkenini kullanın.</span><span class="sxs-lookup"><span data-stu-id="944a1-143">To change the depth of properties expanded, use the `-Depth` argument.</span></span> <span data-ttu-id="944a1-144">Varsayılan olarak, genişletme derinliği `2` olur.</span><span class="sxs-lookup"><span data-stu-id="944a1-144">By default, the expansion depth is `2`.</span></span>

```azurepowershell-interactive
Get-AzVM|ConvertTo-JSON
```

<span data-ttu-id="944a1-145">Aşağıdaki çıkışta bazı alanlar kaldırılmıştır.</span><span class="sxs-lookup"><span data-stu-id="944a1-145">The following output has some fields removed.</span></span>

```output
[
    {
        "ResourceGroupName":  "QUERYEXAMPLE",
        "Id":  "/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM",
        "VmId":  "...",
        "Name":  "ExampleLinuxVM",
        "Type":  "Microsoft.Compute/virtualMachines",
        "Location":  "westus2",
        ...
        "OSProfile":  {
                          "ComputerName":  "ExampleLinuxVM",
                          "AdminUsername":  "...",
                          "AdminPassword":  null,
                          "CustomData":  null,
                          "WindowsConfiguration":  null,
                          "LinuxConfiguration":  "Microsoft.Azure.Management.Compute.Models.LinuxConfiguration",
                          "Secrets":  "",
                          "AllowExtensionOperations":  true
                      },
        "Plan":  null,
        "ProvisioningState":  "Succeeded",
        "StorageProfile":  {
                               "ImageReference":  "Microsoft.Azure.Management.Compute.Models.ImageReference",
                               "OsDisk":  "Microsoft.Azure.Management.Compute.Models.OSDisk",
                               "DataDisks":  ""
                           },
        "DisplayHint":  0,
        "Identity":  null,
        "Zones":  [

                  ],
        "FullyQualifiedDomainName":  null,
        "AdditionalCapabilities":  null,
        "RequestId":  "...",
        "StatusCode":  200
    },
    ...
]
```

### <a name="conversion-to-xml"></a><span data-ttu-id="944a1-146">XML'ye dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-146">Conversion to XML</span></span>

<span data-ttu-id="944a1-147">`ConvertTo-XML` cmdlet'i Azure PowerShell yanıt nesnesini saf XML nesnesine dönüştürür ve bu nesne PowerShell içinde diğer herhangi bir XML nesnesi gibi işlenebilir.</span><span class="sxs-lookup"><span data-stu-id="944a1-147">The `ConvertTo-XML` cmdlet converts the Azure PowerShell response object into a pure XML object, which can be handled like any other XML object within PowerShell.</span></span> 

```azurepowershell-interactive
Get-AzVM | ConvertTo-XML
```

```output
xml                            Objects
---                            -------
version="1.0" encoding="utf-8" Objects
```

### <a name="conversion-to-html"></a><span data-ttu-id="944a1-148">HTML'ye dönüştürme</span><span class="sxs-lookup"><span data-stu-id="944a1-148">Conversion to HTML</span></span>

<span data-ttu-id="944a1-149">Bir nesnenin HTML'ye dönüştürülmesi, HTML tablosu olarak işlenebilecek bir çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="944a1-149">Converting an object to HTML produces output that will be rendered as an HTML table.</span></span> <span data-ttu-id="944a1-150">HTML'nin işlenmesi, tarayıcınızın genişlik bilgisi içermeyen tabloları işleme davranışına bağlı olacaktır.</span><span class="sxs-lookup"><span data-stu-id="944a1-150">Rendering of the HTML will depend on your browser behavior for rendering tables which contain no width information.</span></span>
<span data-ttu-id="944a1-151">Hiçbir özel sınıf nesnesi genişletilmez.</span><span class="sxs-lookup"><span data-stu-id="944a1-151">No custom class objects are expanded.</span></span>

```azurepowershell-interactive
Get-AzVM | ConvertTo-HTML
```

```output
<!DOCTYPE html PUBLIC "-//W3C//DTD XHTML 1.0 Strict//EN"  "http://www.w3.org/TR/xhtml1/DTD/xhtml1-strict.dtd">
<html xmlns="http://www.w3.org/1999/xhtml">
<head>
<title>HTML TABLE</title>
</head><body>
<table>
<colgroup><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/><col/></colgroup>
<tr><th>ResourceGroupName</th><th>Id</th><th>VmId</th><th>Name</th><th>Type</th><th>Location</th><th>LicenseType</th><th>Tags</th><th>AvailabilitySetReference</th><th>DiagnosticsProfile</th><th>Extensions</th><th>HardwareProfile</th><th>InstanceView</th><th>NetworkProfile</th><th>OSProfile</th><th>Plan</th><th>ProvisioningState</th><th>StorageProfile</th><th>DisplayHint</th><th>Identity</th><th>Zones</th><th>FullyQualifiedDomainName</th><th>AdditionalCapabilities</th><th>RequestId</th><th>StatusCode</th></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/ExampleLinuxVM</td><td>...</td><td>ExampleLinuxVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/RHELExample</td><td>...</td><td>RHELExample</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
<tr><td>QUERYEXAMPLE</td><td>/subscriptions/.../resourceGroups/QUERYEXAMPLE/providers/Microsoft.Compute/virtualMachines/WinExampleVM</td><td>...</td><td>WinExampleVM</td><td>Microsoft.Compute/virtualMachines</td><td>westus2</td><td></td><td>System.Collections.Generic.Dictionary`2[System.String,System.String]</td><td></td><td></td><td>System.Collections.Generic.List`1[Microsoft.Azure.Management.Compute.Models.VirtualMachineExtension]</td><td>Microsoft.Azure.Management.Compute.Models.HardwareProfile</td><td></td><td>Microsoft.Azure.Management.Compute.Models.NetworkProfile</td><td>Microsoft.Azure.Management.Compute.Models.OSProfile</td><td></td><td>Succeeded</td><td>Microsoft.Azure.Management.Compute.Models.StorageProfile</td><td>Compact</td><td></td><td>System.Collections.Generic.List`1[System.String]</td><td></td><td></td><td>...</td><td>OK</td></tr>
</table>
</body></html>
```

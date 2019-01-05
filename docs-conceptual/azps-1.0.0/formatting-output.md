---
title: Azure PowerShell cmdlet'inin çıkışını biçimlendirme
description: Azure PowerShell için cmdlet çıkışını biçimlendirme.
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 12/13/2018
ms.openlocfilehash: 4b2c5c46c59164982d0665d68836b7f1b4165b33
ms.sourcegitcommit: 797c18f93aaa495ef005993b2e202d7378588dfa
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 12/19/2018
ms.locfileid: "53595147"
---
# <a name="format-azurepowershell-cmdlet-output"></a><span data-ttu-id="5c5fd-103">Azure PowerShell cmdlet'inin çıkışını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="5c5fd-103">Format AzurePowerShell cmdlet output</span></span>

<span data-ttu-id="5c5fd-104">Varsayılan olarak her Azure PowerShell cmdlet’i, cmdlet’in okunmasını kolaylaştıran önceden tanımlanmış çıktı biçimlendirmesine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-104">By default each Azure PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="5c5fd-105">PowerShell, çıktıyı ayarlama veya cmdlet çıktısını aşağıdaki cmdlet’ler ile farklı bir biçime dönüştürme esnekliğini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="5c5fd-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="5c5fd-106">Biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="5c5fd-106">Formatting</span></span>      | <span data-ttu-id="5c5fd-107">Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="5c5fd-107">Conversion</span></span>       |
|-----------------|------------------|
| [<span data-ttu-id="5c5fd-108">Format-Custom</span><span class="sxs-lookup"><span data-stu-id="5c5fd-108">Format-Custom</span></span>](/powershell/module/microsoft.powershell.utility/format-custom) | [<span data-ttu-id="5c5fd-109">ConvertTo-Csv</span><span class="sxs-lookup"><span data-stu-id="5c5fd-109">ConvertTo-Csv</span></span>](/powershell/module/microsoft.powershell.utility/convertto-csv)  |
| [<span data-ttu-id="5c5fd-110">Format-List</span><span class="sxs-lookup"><span data-stu-id="5c5fd-110">Format-List</span></span>](/powershell/module/microsoft.powershell.utility/format-list)   | [<span data-ttu-id="5c5fd-111">ConvertTo-Html</span><span class="sxs-lookup"><span data-stu-id="5c5fd-111">ConvertTo-Html</span></span>](/powershell/module/microsoft.powershell.utility/convertto-html) |
| [<span data-ttu-id="5c5fd-112">Format-Table</span><span class="sxs-lookup"><span data-stu-id="5c5fd-112">Format-Table</span></span>](/powershell/module/microsoft.powershell.utility/format-table)  | [<span data-ttu-id="5c5fd-113">ConvertTo-Json</span><span class="sxs-lookup"><span data-stu-id="5c5fd-113">ConvertTo-Json</span></span>](/powershell/module/microsoft.powershell.utility/convertto-json) |
| [<span data-ttu-id="5c5fd-114">Format-Wide</span><span class="sxs-lookup"><span data-stu-id="5c5fd-114">Format-Wide</span></span>](/powershell/module/microsoft.powershell.utility/format-wide)   | [<span data-ttu-id="5c5fd-115">ConvertTo-Xml</span><span class="sxs-lookup"><span data-stu-id="5c5fd-115">ConvertTo-Xml</span></span>](/powershell/module/microsoft.powershell.utility/convertto-xml)  |

## <a name="format-examples"></a><span data-ttu-id="5c5fd-116">Biçimlendirme örnekleri</span><span class="sxs-lookup"><span data-stu-id="5c5fd-116">Format examples</span></span>

<span data-ttu-id="5c5fd-117">Bu örnekte, varsayılan aboneliğimizdeki Azure VM'lerinin listesini alırız.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-117">In this example, we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="5c5fd-118">`Get-AzVM` komutu, varsayılan olarak bir tablo biçiminde çıkış oluşturur.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-118">The `Get-AzVM` command defaults output into a table format.</span></span>

```azurepowershell-interactive
Get-AzVM
```

```output
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="5c5fd-119">Döndürülen sütunları sınırlamak isterseniz `Format-Table` cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-119">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="5c5fd-120">Aşağıdaki örnekte, aynı sanal makine listesini alıyoruz ancak çıktıyı yalnızca VM’nin adı, kaynak grubu ve VM’nin konumu ile sınırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-120">In the following example, we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="5c5fd-121">`-Autosize` parametresi, sütunları veri boyutuna göre boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-121">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```azurepowershell-interactive
Get-AzVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```output
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="5c5fd-122">Çıkış bir liste olarak da biçimlendirilebilir.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-122">Output can also be formatted into a list.</span></span> <span data-ttu-id="5c5fd-123">Aşağıdaki örnekte `Format-List` cmdlet’i kullanılarak bunun nasıl yapılacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-123">The following example shows this using the`Format-List` cmdlet.</span></span>

```azurepowershell-interactive
Get-AzVM | Format-List Name,VmId,Location,ResourceGroupName
```

```output
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="convert-to-other-data-types"></a><span data-ttu-id="5c5fd-124">Diğer veri türlerine dönüştürme</span><span class="sxs-lookup"><span data-stu-id="5c5fd-124">Convert to other data types</span></span>

<span data-ttu-id="5c5fd-125">PowerShell, komut çıkışını alıp birden çok veri biçimine dönüştürmeye olanak tanır.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-125">PowerShell also allows taking command output and converting it into multiple data formats.</span></span> <span data-ttu-id="5c5fd-126">Aşağıdaki örnekte, `Select-Object` cmdlet’i kullanılarak aboneliğimizdeki sanal makinelerin öznitelikleri alınır ve veritabanı veya elektronik tabloya kolayca aktarılabilmesi için çıkış CSV biçimine dönüştürülür.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-126">In the following example, the `Select-Object` cmdlet is used to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```azurepowershell-interactive
Get-AzVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```output
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="5c5fd-127">Çıkış JSON biçimine de dönüştürülebilir.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-127">Output can also be converted into the JSON format.</span></span>  <span data-ttu-id="5c5fd-128">Aşağıdaki örnekte aynı VM listesi oluşturulur, ancak çıktı biçimi JSON olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="5c5fd-128">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```azurepowershell-interactive
Get-AzVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```output
[
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610",
        "VmId":  "33422f9b-e339-4704-bad8-dbe094585496",
        "Name":  "MyUnbuntu1610",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    },
    {
        "ResourceGroupName":  "MYWESTEURG",
        "Id":  "/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTEURG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM",
        "VmId":  "4650c755-fc2b-4fc7-a5bc-298d5c00808f",
        "Name":  "MyWin2016VM",
        "Location":  "westeurope",
        "ProvisioningState":  "Succeeded"
    }
]
```
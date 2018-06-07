---
title: Sorgu sonuçlarını biçimlendirme | Microsoft Docs
description: Azure’daki kaynakları sorgulama ve sonuçları biçimlendirme.
services: azure
author: sptramer
ms.author: sttramer
manager: carmonm
ms.devlang: powershell
ms.topic: conceptual
ms.date: 03/30/2017
ms.openlocfilehash: 1c576aba64d2afd1bd11a0d260479e7761cb82f1
ms.sourcegitcommit: 2eea03b7ac19ad6d7c8097743d33c7ddb9c4df77
ms.translationtype: HT
ms.contentlocale: tr-TR
ms.lasthandoff: 06/06/2018
ms.locfileid: "34819584"
---
# <a name="formatting-query-results"></a><span data-ttu-id="0e156-103">Sorgu sonuçlarını biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="0e156-103">Formatting query results</span></span>

<span data-ttu-id="0e156-104">Varsayılan olarak her PowerShell cmdlet’i, cmdlet’in okunmasını kolaylaştıran önceden tanımlanmış çıktı biçimlendirmesine sahiptir.</span><span class="sxs-lookup"><span data-stu-id="0e156-104">By default each PowerShell cmdlet has predefined formatting of output making it easy to read.</span></span>  <span data-ttu-id="0e156-105">PowerShell, çıktıyı ayarlama veya cmdlet çıktısını aşağıdaki cmdlet’ler ile farklı bir biçime dönüştürme esnekliğini de sağlar:</span><span class="sxs-lookup"><span data-stu-id="0e156-105">PowerShell also provides the flexibility to adjust the output or convert the cmdlet output to a different format with the following cmdlets:</span></span>

| <span data-ttu-id="0e156-106">Biçimlendirme</span><span class="sxs-lookup"><span data-stu-id="0e156-106">Formatting</span></span>      | <span data-ttu-id="0e156-107">Dönüştürme</span><span class="sxs-lookup"><span data-stu-id="0e156-107">Conversion</span></span>       |
|-----------------|------------------|
| `Format-Custom` | `ConvertTo-Csv`  |
| `Format-List`   | `ConvertTo-Html` |
| `Format-Table`  | `ConvertTo-Json` |
| `Format-Wide`   | `ConvertTo-Xml`  |

## <a name="formatting-examples"></a><span data-ttu-id="0e156-108">Biçimlendirme örnekleri</span><span class="sxs-lookup"><span data-stu-id="0e156-108">Formatting examples</span></span>

<span data-ttu-id="0e156-109">Bu örnekte, varsayılan aboneliğimizdeki Azure VM'lerinin listesini alırız.</span><span class="sxs-lookup"><span data-stu-id="0e156-109">In this example we get a list of Azure VMs in our default subscription.</span></span>  <span data-ttu-id="0e156-110">Get-AzureRmVM komutu, varsayılan olarak bir tablo biçiminde çıktı oluşturur.</span><span class="sxs-lookup"><span data-stu-id="0e156-110">The Get-AzureRmVM command defaults output into a table format.</span></span>

```powershell
Get-AzureRmVM
```

```
ResourceGroupName          Name   Location          VmSize  OsType              NIC ProvisioningState
-----------------          ----   --------          ------  ------              --- -----------------
MYWESTEURG        MyUnbuntu1610 westeurope Standard_DS1_v2   Linux myunbuntu1610980         Succeeded
MYWESTEURG          MyWin2016VM westeurope Standard_DS1_v2 Windows   mywin2016vm880         Succeeded
```

<span data-ttu-id="0e156-111">Döndürülen sütunları sınırlamak isterseniz `Format-Table` cmdlet’ini kullanabilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e156-111">If you would like to limit the columns returned you can use the `Format-Table` cmdlet.</span></span> <span data-ttu-id="0e156-112">Aşağıdaki örnekte, aynı sanal makine listesini alıyoruz ancak çıktıyı yalnızca VM’nin adı, kaynak grubu ve VM’nin konumu ile sınırlıyoruz.</span><span class="sxs-lookup"><span data-stu-id="0e156-112">In the following example we get the same list of virtual machines but restrict the output to just the name of the VM, the resource group, and the location of the VM.</span></span>  <span data-ttu-id="0e156-113">`-Autosize` parametresi, sütunları veri boyutuna göre boyutlandırır.</span><span class="sxs-lookup"><span data-stu-id="0e156-113">The `-Autosize` parameter sizes the columns according to the size of the data.</span></span>

```powershell
Get-AzureRmVM | Format-Table Name,ResourceGroupName,Location -AutoSize
```

```
Name          ResourceGroupName Location
----          ----------------- --------
MyUnbuntu1610 MYWESTEURG        westeurope
MyWin2016VM   MYWESTEURG        westeurope
```

<span data-ttu-id="0e156-114">İsterseniz bilgileri bir liste biçiminde görüntüleyebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e156-114">If you would prefer you can view information in a list format.</span></span> <span data-ttu-id="0e156-115">Aşağıdaki örnekte `Format-List` cmdlet’i kullanılarak bunun nasıl yapılacağı gösterilir.</span><span class="sxs-lookup"><span data-stu-id="0e156-115">The following example shows this using the`Format-List` cmdlet.</span></span>

```powershell
Get-AzureRmVM | Format-List Name,VmId,Location,ResourceGroupName
```

```
Name              : MyUnbuntu1610
VmId              : 33422f9b-e339-4704-bad8-dbe094585496
Location          : westeurope
ResourceGroupName : MYWESTEURG

Name              : MyWin2016VM
VmId              : 4650c755-fc2b-4fc7-a5bc-298d5c00808f
Location          : westeurope
ResourceGroupName : MYWESTEURG
```

## <a name="converting-to-other-data-types"></a><span data-ttu-id="0e156-116">Diğer veri türlerine dönüştürme</span><span class="sxs-lookup"><span data-stu-id="0e156-116">Converting to other data types</span></span>

<span data-ttu-id="0e156-117">PowerShell, gereksinimlerinizi karşılamak için kullanabileceğiniz birden çok çıktı biçimi de sunar.</span><span class="sxs-lookup"><span data-stu-id="0e156-117">PowerShell also offers multiple output format you can use to meet your needs.</span></span>  <span data-ttu-id="0e156-118">Aşağıdaki örnekte, `Select-Object` cmdlet’ini kullanarak aboneliğimizdeki sanal makinelerin özniteliklerini alır ve çıktıyı bir veritabanı ya da elektronik tabloya kolayca aktarılabilmesi için CSV biçimine dönüştürürüz.</span><span class="sxs-lookup"><span data-stu-id="0e156-118">In the following example we use the `Select-Object` cmdlet to get attributes of the virtual machines in our subscription and convert the output to CSV format for easy import into a database or spreadsheet.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Csv -NoTypeInformation
```

```
"ResourceGroupName","Id","VmId","Name","Location","ProvisioningState"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyUnbuntu1610","33422f9b-e339-4704-bad8-dbe094585496","MyUnbuntu1610","westeurope","Succeeded"
"MYWESTUERG","/subscriptions/XXXXXXXX-XXXX-XXXX-XXXX-XXXXXXXXXXXX/resourceGroups/MYWESTUERG/providers/Microsoft.Compute/virtualMachines/MyWin2016VM","4650c755-fc2b-4fc7-a5bc-298d5c00808f","MyWin2016VM","westeurope","Succeeded"
```

<span data-ttu-id="0e156-119">Çıktıyı JSON biçimine de dönüştürebilirsiniz.</span><span class="sxs-lookup"><span data-stu-id="0e156-119">You can also convert the output into JSON format.</span></span>  <span data-ttu-id="0e156-120">Aşağıdaki örnekte aynı VM listesi oluşturulur, ancak çıktı biçimi JSON olarak değiştirilir.</span><span class="sxs-lookup"><span data-stu-id="0e156-120">The following example creates the same list of VMs but changes the output format to JSON.</span></span>

```powershell
Get-AzureRmVM | Select-Object ResourceGroupName,Id,VmId,Name,Location,ProvisioningState | ConvertTo-Json
```

```
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

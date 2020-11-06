---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: a6f2ed82835cca252f905cb53c5ddd9c8530900a
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594129"
---
# <span data-ttu-id="b65d3-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b65d3-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="b65d3-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="b65d3-102">SYNOPSIS</span></span>
<span data-ttu-id="b65d3-103">Sanal makinedeki SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="b65d3-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="b65d3-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [<CommonParameters>]
```

## <span data-ttu-id="b65d3-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="b65d3-105">DESCRIPTION</span></span>
<span data-ttu-id="b65d3-106">**Get-AzureRmVMSqlServerExtension** cmdlet 'ı, SQL Server altyapısının bir sanal makinede hizmet (IaaS) Aracısı olarak ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="b65d3-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="b65d3-107">EXAMPLES</span></span>

### <span data-ttu-id="b65d3-108">Örnek 1: sanal makinedeki SQL Server uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="b65d3-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b65d3-109">Bu komut, ContosoVM07 adındaki bir sanal makinede SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="b65d3-110">Örnek 2: ardışık düzeni kullanarak ayarları alma</span><span class="sxs-lookup"><span data-stu-id="b65d3-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzureRmVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzureRmVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b65d3-111">Bu komut, Get-AzureRmVM cmdlet 'ini kullanarak hizmet Service08 ContosoVM22 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="b65d3-112">Komut, ardışık düzen işlecini kullanarak sonuçları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="b65d3-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="b65d3-113">Current komutu, bu sanal makinede SQL Server IaaS aracısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="b65d3-114">Örnek 3: belirli bir SQL Server sürümünün ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="b65d3-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzureRmVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="b65d3-115">Bu komut, ContosoVM07 adındaki sanal makinedeki SQL Server uzantısının 1,0 sürüm ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="b65d3-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="b65d3-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="b65d3-116">PARAMETERS</span></span>

### <span data-ttu-id="b65d3-117">-Ad</span><span class="sxs-lookup"><span data-stu-id="b65d3-117">-Name</span></span>
<span data-ttu-id="b65d3-118">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b65d3-118">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65d3-119">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="b65d3-119">-ResourceGroupName</span></span>
<span data-ttu-id="b65d3-120">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b65d3-120">Specifies the name of the resource group of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 0
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65d3-121">-VMName</span><span class="sxs-lookup"><span data-stu-id="b65d3-121">-VMName</span></span>
<span data-ttu-id="b65d3-122">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="b65d3-122">Specifies the name of the virtual machine.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: 

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="b65d3-123">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="b65d3-123">CommonParameters</span></span>
<span data-ttu-id="b65d3-124">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="b65d3-124">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="b65d3-125">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="b65d3-125">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="b65d3-126">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="b65d3-126">INPUTS</span></span>

### <span data-ttu-id="b65d3-127">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="b65d3-127">None</span></span>
<span data-ttu-id="b65d3-128">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="b65d3-128">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="b65d3-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="b65d3-129">OUTPUTS</span></span>

## <span data-ttu-id="b65d3-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="b65d3-130">NOTES</span></span>

## <span data-ttu-id="b65d3-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="b65d3-131">RELATED LINKS</span></span>

[<span data-ttu-id="b65d3-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="b65d3-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="b65d3-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b65d3-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="b65d3-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="b65d3-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help-Help.xml
Module Name: Az.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azvmsqlserverextension
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/Azs-tzl/src/Compute/Compute/help/Get-AzVMSqlServerExtension.md
ms.openlocfilehash: a3570a65e5c4f6aa305c4123188d094d9bd4545c
ms.sourcegitcommit: 4c61442a2df1cee633ce93cad9f6bc793803baa2
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 04/16/2020
ms.locfileid: "93937005"
---
# <span data-ttu-id="9f5fa-101">Get-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9f5fa-101">Get-AzVMSqlServerExtension</span></span>

## <span data-ttu-id="9f5fa-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="9f5fa-102">SYNOPSIS</span></span>
<span data-ttu-id="9f5fa-103">Sanal makinedeki SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

## <span data-ttu-id="9f5fa-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="9f5fa-104">SYNTAX</span></span>

```
Get-AzVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="9f5fa-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="9f5fa-105">DESCRIPTION</span></span>
<span data-ttu-id="9f5fa-106">**Get-AzVMSqlServerExtension** cmdlet 'ı, SQL Server altyapısının bir sanal makinede hizmet (IaaS) Aracısı ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-106">The **Get-AzVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="9f5fa-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="9f5fa-107">EXAMPLES</span></span>

### <span data-ttu-id="9f5fa-108">Örnek 1: sanal makinedeki SQL Server uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="9f5fa-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9f5fa-109">Bu komut, ContosoVM07 adındaki bir sanal makinede SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="9f5fa-110">Örnek 2: ardışık düzeni kullanarak ayarları alma</span><span class="sxs-lookup"><span data-stu-id="9f5fa-110">Example 2: Get the settings by using the pipeline</span></span>
```
PS C:\> Get-AzVM -ServiceName "Service08" -Name "ContosoVM22" | Get-AzVMSqlServerExtension
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9f5fa-111">Bu komut, Get-AzVM cmdlet 'ini kullanarak hizmet Service08 ContosoVM22 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzVM cmdlet.</span></span>
<span data-ttu-id="9f5fa-112">Komut, ardışık düzen işlecini kullanarak sonuçları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="9f5fa-113">Current komutu, bu sanal makinede SQL Server IaaS aracısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="9f5fa-114">Örnek 3: belirli bir SQL Server sürümünün ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="9f5fa-114">Example 3: Get the settings of specific SQL Server version</span></span>
```
PS C:\> Get-AzVMSqlServerExtension -ResourceGroupName "ResourceGroup11" -VMName "ContosoVM07" -Version "1.0"
ExtensionName        : SqlIaaSAgent
Publisher            : Microsoft.SqlServer.Management
Version              : 1.0
State                : Enable
RoleName             : VMName
AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="9f5fa-115">Bu komut, ContosoVM07 adındaki sanal makinedeki SQL Server uzantısının 1,0 sürüm ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="9f5fa-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="9f5fa-116">PARAMETERS</span></span>

### <span data-ttu-id="9f5fa-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="9f5fa-117">-DefaultProfile</span></span>
<span data-ttu-id="9f5fa-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="9f5fa-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="9f5fa-119">-Name</span></span>
<span data-ttu-id="9f5fa-120">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-120">Specifies the name of the SQL Server the extension.</span></span>

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

### <span data-ttu-id="9f5fa-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="9f5fa-121">-ResourceGroupName</span></span>
<span data-ttu-id="9f5fa-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="9f5fa-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="9f5fa-123">-VMName</span></span>
<span data-ttu-id="9f5fa-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="9f5fa-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="9f5fa-125">CommonParameters</span></span>
<span data-ttu-id="9f5fa-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="9f5fa-127">Daha fazla bilgi için bkz about_CommonParameters ( http://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="9f5fa-127">For more information, see about_CommonParameters (http://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="9f5fa-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="9f5fa-128">INPUTS</span></span>

### <span data-ttu-id="9f5fa-129">Yabilirsiniz</span><span class="sxs-lookup"><span data-stu-id="9f5fa-129">None</span></span>
<span data-ttu-id="9f5fa-130">Bu cmdlet hiçbir girişi kabul etmez.</span><span class="sxs-lookup"><span data-stu-id="9f5fa-130">This cmdlet does not accept any input.</span></span>

## <span data-ttu-id="9f5fa-131">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="9f5fa-131">OUTPUTS</span></span>

### <span data-ttu-id="9f5fa-132">Microsoft. Azure. Commands. COMPUTE. Virtu</span><span class="sxs-lookup"><span data-stu-id="9f5fa-132">Microsoft.Azure.Commands.Compute.VirtualMachineSqlServerExtensionContext</span></span>

## <span data-ttu-id="9f5fa-133">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="9f5fa-133">NOTES</span></span>

## <span data-ttu-id="9f5fa-134">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="9f5fa-134">RELATED LINKS</span></span>

[<span data-ttu-id="9f5fa-135">Get-AzVM</span><span class="sxs-lookup"><span data-stu-id="9f5fa-135">Get-AzVM</span></span>](./Get-AzVM.md)

[<span data-ttu-id="9f5fa-136">Remove-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9f5fa-136">Remove-AzVMSqlServerExtension</span></span>](./Remove-AzVMSqlServerExtension.md)

[<span data-ttu-id="9f5fa-137">Set-AzVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="9f5fa-137">Set-AzVMSqlServerExtension</span></span>](./Set-AzVMSqlServerExtension.md)



---
external help file: Microsoft.Azure.Commands.Compute.dll-Help.xml
Module Name: AzureRM.Compute
ms.assetid: CAA3E6A9-7E1A-4D57-A269-0B2D3D9C3BEC
online version: ''
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/preview/src/ResourceManager/Compute/Stack/Commands.Compute/help/Get-AzureRMVMSqlServerExtension.md
ms.openlocfilehash: 94c93410692c71b16150b2078f764f5b96c71e6e
ms.sourcegitcommit: f599b50d5e980197d1fca769378df90a842b42a1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 08/20/2020
ms.locfileid: "93594315"
---
# <span data-ttu-id="6feb5-101">Get-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6feb5-101">Get-AzureRmVMSqlServerExtension</span></span>

## <span data-ttu-id="6feb5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6feb5-102">SYNOPSIS</span></span>
<span data-ttu-id="6feb5-103">Sanal makinedeki SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-103">Gets the settings for a SQL Server extension on a virtual machine.</span></span>

[!INCLUDE [migrate-to-az-banner](../../includes/migrate-to-az-banner.md)]

## <span data-ttu-id="6feb5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6feb5-104">SYNTAX</span></span>

```
Get-AzureRmVMSqlServerExtension [-ResourceGroupName] <String> [-VMName] <String> [[-Name] <String>]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6feb5-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="6feb5-105">DESCRIPTION</span></span>
<span data-ttu-id="6feb5-106">**Get-AzureRmVMSqlServerExtension** cmdlet 'ı, SQL Server altyapısının bir sanal makinede hizmet (IaaS) Aracısı olarak ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-106">The **Get-AzureRmVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a virtual machine.</span></span>

## <span data-ttu-id="6feb5-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6feb5-107">EXAMPLES</span></span>

### <span data-ttu-id="6feb5-108">Örnek 1: sanal makinedeki SQL Server uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="6feb5-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
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

<span data-ttu-id="6feb5-109">Bu komut, ContosoVM07 adındaki bir sanal makinede SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-109">This command gets the settings of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

### <span data-ttu-id="6feb5-110">Örnek 2: ardışık düzeni kullanarak ayarları alma</span><span class="sxs-lookup"><span data-stu-id="6feb5-110">Example 2: Get the settings by using the pipeline</span></span>
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

<span data-ttu-id="6feb5-111">Bu komut, Get-AzureRmVM cmdlet 'ini kullanarak hizmet Service08 ContosoVM22 adındaki sanal makineyi alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-111">This command gets the virtual machine named ContosoVM22 on the service Service08 by using the Get-AzureRmVM cmdlet.</span></span>
<span data-ttu-id="6feb5-112">Komut, ardışık düzen işlecini kullanarak sonuçları geçerli cmdlet 'e geçirir.</span><span class="sxs-lookup"><span data-stu-id="6feb5-112">The command passes the results to the current cmdlet by using the pipeline operator.</span></span>

<span data-ttu-id="6feb5-113">Current komutu, bu sanal makinede SQL Server IaaS aracısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-113">The current command gets the settings of the SQL Server IaaS Agent on that virtual machine.</span></span>

### <span data-ttu-id="6feb5-114">Örnek 3: belirli bir SQL Server sürümünün ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="6feb5-114">Example 3: Get the settings of specific SQL Server version</span></span>
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

<span data-ttu-id="6feb5-115">Bu komut, ContosoVM07 adındaki sanal makinedeki SQL Server uzantısının 1,0 sürüm ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="6feb5-115">This command gets the settings of version 1.0 of the SQL Server extension on a virtual machine named ContosoVM07.</span></span>

## <span data-ttu-id="6feb5-116">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6feb5-116">PARAMETERS</span></span>

### <span data-ttu-id="6feb5-117">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6feb5-117">-DefaultProfile</span></span>
<span data-ttu-id="6feb5-118">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6feb5-118">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

```yaml
Type: Microsoft.Azure.Commands.Common.Authentication.Abstractions.IAzureContextContainer
Parameter Sets: (All)
Aliases: AzureRmContext, AzureCredential

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6feb5-119">-Ad</span><span class="sxs-lookup"><span data-stu-id="6feb5-119">-Name</span></span>
<span data-ttu-id="6feb5-120">Uzantının adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6feb5-120">Specifies the name of the SQL Server the extension.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: 

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6feb5-121">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6feb5-121">-ResourceGroupName</span></span>
<span data-ttu-id="6feb5-122">Sanal makinenin kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6feb5-122">Specifies the name of the resource group of the virtual machine.</span></span>

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

### <span data-ttu-id="6feb5-123">-VMName</span><span class="sxs-lookup"><span data-stu-id="6feb5-123">-VMName</span></span>
<span data-ttu-id="6feb5-124">Sanal makinenin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6feb5-124">Specifies the name of the virtual machine.</span></span>

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

### <span data-ttu-id="6feb5-125">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6feb5-125">CommonParameters</span></span>
<span data-ttu-id="6feb5-126">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6feb5-126">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6feb5-127">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="6feb5-127">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6feb5-128">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6feb5-128">INPUTS</span></span>

## <span data-ttu-id="6feb5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6feb5-129">OUTPUTS</span></span>

## <span data-ttu-id="6feb5-130">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6feb5-130">NOTES</span></span>

## <span data-ttu-id="6feb5-131">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6feb5-131">RELATED LINKS</span></span>

[<span data-ttu-id="6feb5-132">Get-AzureRmVM</span><span class="sxs-lookup"><span data-stu-id="6feb5-132">Get-AzureRmVM</span></span>](./Get-AzureRmVM.md)

[<span data-ttu-id="6feb5-133">Remove-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6feb5-133">Remove-AzureRmVMSqlServerExtension</span></span>](./Remove-AzureRMVMSqlServerExtension.md)

[<span data-ttu-id="6feb5-134">Set-AzureRmVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="6feb5-134">Set-AzureRmVMSqlServerExtension</span></span>](./Set-AzureRMVMSqlServerExtension.md)



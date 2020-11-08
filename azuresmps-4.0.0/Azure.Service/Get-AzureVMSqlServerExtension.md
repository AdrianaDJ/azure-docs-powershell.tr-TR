---
external help file: Microsoft.WindowsAzure.Commands.ServiceManagement.dll-Help.xml
ms.assetid: 8CE8F4E9-93D4-41E5-8B43-F886C018D9FB
online version: ''
schema: 2.0.0
ms.openlocfilehash: 06681544df4974a1ee906552af96302698e88d74
ms.sourcegitcommit: 56ed085a868afa8263f8eb0f755b5822f5c29532
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 07/18/2020
ms.locfileid: "94105530"
---
# <span data-ttu-id="5bbac-101">Get-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bbac-101">Get-AzureVMSqlServerExtension</span></span>

## <span data-ttu-id="5bbac-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="5bbac-102">SYNOPSIS</span></span>
<span data-ttu-id="5bbac-103">Belirli bir sanal makinede SQL Server IaaS aracısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bbac-103">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="5bbac-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="5bbac-104">SYNTAX</span></span>

```
Get-AzureVMSqlServerExtension -VM <IPersistentVM> [-Profile <AzureSMProfile>]
 [-InformationAction <ActionPreference>] [-InformationVariable <String>] [<CommonParameters>]
```

## <span data-ttu-id="5bbac-105">Tanım</span><span class="sxs-lookup"><span data-stu-id="5bbac-105">DESCRIPTION</span></span>
<span data-ttu-id="5bbac-106">**Get-AzureVMSqlServerExtension** cmdlet 'ı, SQL Server altyapısının belirli bir sanal makinede hizmet (IaaS) Aracısı olarak ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bbac-106">The **Get-AzureVMSqlServerExtension** cmdlet gets the settings of the SQL Server infrastructure as a service (IaaS) Agent on a particular virtual machine.</span></span>

## <span data-ttu-id="5bbac-107">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="5bbac-107">EXAMPLES</span></span>

### <span data-ttu-id="5bbac-108">Örnek 1: sanal makinedeki SQL Server uzantısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5bbac-108">Example 1: Get the settings of a SQL Server extension on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension-VM $VM
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="5bbac-109">Belirli bir sanal makinedeki SQL Server uzantısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bbac-109">Gets the settings of the SQL Server extension on a particular virtual machine.</span></span>

### <span data-ttu-id="5bbac-110">Örnek 2: sanal makinede SQL Server IaaS aracısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5bbac-110">Example 2: Get the settings of a SQL Server IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVM -ServiceName "Service" -Name "VMName" | Get-AzureVMSqlServerExtension
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="5bbac-111">Piped girişi kullanarak belirli bir sanal makinede SQL Server IaaS aracısının ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bbac-111">Gets the settings of the SQL Server IaaS Agent on a particular virtual machine using piped input.</span></span>

### <span data-ttu-id="5bbac-112">Örnek 3: sanal makinedeki belirli SQL Server sürümü IaaS aracısının ayarlarını alma</span><span class="sxs-lookup"><span data-stu-id="5bbac-112">Example 3: Get the settings of specific SQL Server version IaaS Agent on a virtual machine</span></span>
```
PS C:\> Get-AzureVMSqlServerExtension -VM $VM -Version "1.0"
          ExtensionName        : SqlIaaSAgent
          Publisher            : Microsoft.SqlServer.Management
          Version              : 1.0
          State                : Enable
          RoleName             : VMName
          AutoPatchingSettings : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoPatchingSettings
          AutoBackupSettings   : Microsoft.WindowsAzure.Commands.ServiceManagement.IaaS.Extensions.AutoBackupSettings
```

<span data-ttu-id="5bbac-113">Bu komut, bir sanal makinede SQL Server IaaS aracısının belirli sürümünün ayarlarını alır.</span><span class="sxs-lookup"><span data-stu-id="5bbac-113">This command gets the settings of the particular version of SQL Server IaaS Agent on a virtual machine.</span></span>

## <span data-ttu-id="5bbac-114">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="5bbac-114">PARAMETERS</span></span>

### <span data-ttu-id="5bbac-115">-Informationaction</span><span class="sxs-lookup"><span data-stu-id="5bbac-115">-InformationAction</span></span>
<span data-ttu-id="5bbac-116">Bu cmdlet 'in bir bilgi olayına nasıl tepki vereceğini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbac-116">Specifies how this cmdlet responds to an information event.</span></span>

<span data-ttu-id="5bbac-117">Bu parametre için kabul edilebilir değerler şunlardır:</span><span class="sxs-lookup"><span data-stu-id="5bbac-117">The acceptable values for this parameter are:</span></span>

- <span data-ttu-id="5bbac-118">'A</span><span class="sxs-lookup"><span data-stu-id="5bbac-118">Continue</span></span>
- <span data-ttu-id="5bbac-119">Manıza</span><span class="sxs-lookup"><span data-stu-id="5bbac-119">Ignore</span></span>
- <span data-ttu-id="5bbac-120">Sorgulamak</span><span class="sxs-lookup"><span data-stu-id="5bbac-120">Inquire</span></span>
- <span data-ttu-id="5bbac-121">Sustlıkdevam</span><span class="sxs-lookup"><span data-stu-id="5bbac-121">SilentlyContinue</span></span>
- <span data-ttu-id="5bbac-122">Durdurduğunuzda</span><span class="sxs-lookup"><span data-stu-id="5bbac-122">Stop</span></span>
- <span data-ttu-id="5bbac-123">Biliriz</span><span class="sxs-lookup"><span data-stu-id="5bbac-123">Suspend</span></span>

```yaml
Type: ActionPreference
Parameter Sets: (All)
Aliases: infa

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-124">-Informationvariable</span><span class="sxs-lookup"><span data-stu-id="5bbac-124">-InformationVariable</span></span>
<span data-ttu-id="5bbac-125">Bir bilgi değişkeni belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbac-125">Specifies an information variable.</span></span>

```yaml
Type: String
Parameter Sets: (All)
Aliases: iv

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-126">-Profil</span><span class="sxs-lookup"><span data-stu-id="5bbac-126">-Profile</span></span>
<span data-ttu-id="5bbac-127">Bu cmdlet 'in okuduğu Azure profilini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbac-127">Specifies the Azure profile from which this cmdlet reads.</span></span>
<span data-ttu-id="5bbac-128">Profil belirtmezseniz, bu cmdlet yerel varsayılan profilden okur.</span><span class="sxs-lookup"><span data-stu-id="5bbac-128">If you do not specify a profile, this cmdlet reads from the local default profile.</span></span>

```yaml
Type: AzureSMProfile
Parameter Sets: (All)
Aliases: 

Required: False
Position: Named
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-129">-VM</span><span class="sxs-lookup"><span data-stu-id="5bbac-129">-VM</span></span>
<span data-ttu-id="5bbac-130">Bu cmdlet 'in ayarları aldığı kalıcı sanal makine nesnesini belirtir.</span><span class="sxs-lookup"><span data-stu-id="5bbac-130">Specifies the persistent virtual machine object that this cmdlet gets settings from.</span></span>

```yaml
Type: IPersistentVM
Parameter Sets: (All)
Aliases: InputObject

Required: True
Position: Named
Default value: None
Accept pipeline input: True (ByPropertyName, ByValue)
Accept wildcard characters: False
```

### <span data-ttu-id="5bbac-131">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="5bbac-131">CommonParameters</span></span>
<span data-ttu-id="5bbac-132">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="5bbac-132">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="5bbac-133">Daha fazla bilgi için bkz about_CommonParameters ( https://go.microsoft.com/fwlink/?LinkID=113216) .</span><span class="sxs-lookup"><span data-stu-id="5bbac-133">For more information, see about_CommonParameters (https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="5bbac-134">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="5bbac-134">INPUTS</span></span>

## <span data-ttu-id="5bbac-135">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="5bbac-135">OUTPUTS</span></span>

## <span data-ttu-id="5bbac-136">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="5bbac-136">NOTES</span></span>

## <span data-ttu-id="5bbac-137">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="5bbac-137">RELATED LINKS</span></span>

[<span data-ttu-id="5bbac-138">Remove-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bbac-138">Remove-AzureVMSqlServerExtension</span></span>](./Remove-AzureVMSqlServerExtension.md)

[<span data-ttu-id="5bbac-139">Set-AzureVMSqlServerExtension</span><span class="sxs-lookup"><span data-stu-id="5bbac-139">Set-AzureVMSqlServerExtension</span></span>](./Set-AzureVMSqlServerExtension.md)



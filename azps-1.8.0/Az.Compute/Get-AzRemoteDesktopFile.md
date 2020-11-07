---
external help file: Microsoft.Azure.PowerShell.Cmdlets.Compute.dll-Help.xml
Module Name: Az.Compute
ms.assetid: E2A56E55-30A3-4A2F-80AE-9D166840909E
online version: https://docs.microsoft.com/en-us/powershell/module/az.compute/get-azremotedesktopfile
schema: 2.0.0
content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
original_content_git_url: https://github.com/Azure/azure-powershell/blob/master/src/Compute/Compute/help/Get-AzRemoteDesktopFile.md
ms.openlocfilehash: 739db22c15678c14e0262c88b83abaa2320edcce
ms.sourcegitcommit: 4d2c178cd6df9151877b08d54c1f4a228dbec9d1
ms.translationtype: MT
ms.contentlocale: tr-TR
ms.lasthandoff: 01/29/2020
ms.locfileid: "93917460"
---
# <span data-ttu-id="6c9e5-101">Get-AzRemoteDesktopFile</span><span class="sxs-lookup"><span data-stu-id="6c9e5-101">Get-AzRemoteDesktopFile</span></span>

## <span data-ttu-id="6c9e5-102">SYNOPSIS</span><span class="sxs-lookup"><span data-stu-id="6c9e5-102">SYNOPSIS</span></span>
<span data-ttu-id="6c9e5-103">Bir. rdp dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-103">Gets an .rdp file.</span></span>

## <span data-ttu-id="6c9e5-104">INDEKI</span><span class="sxs-lookup"><span data-stu-id="6c9e5-104">SYNTAX</span></span>

### <span data-ttu-id="6c9e5-105">İndirin</span><span class="sxs-lookup"><span data-stu-id="6c9e5-105">Download</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [-LocalPath] <String>
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

### <span data-ttu-id="6c9e5-106">Başlatılması</span><span class="sxs-lookup"><span data-stu-id="6c9e5-106">Launch</span></span>
```
Get-AzRemoteDesktopFile [-ResourceGroupName] <String> [-Name] <String> [[-LocalPath] <String>] [-Launch]
 [-DefaultProfile <IAzureContextContainer>] [<CommonParameters>]
```

## <span data-ttu-id="6c9e5-107">Tanım</span><span class="sxs-lookup"><span data-stu-id="6c9e5-107">DESCRIPTION</span></span>
<span data-ttu-id="6c9e5-108">**Get-AzRemoteDesktopFile** cmdlet 'ı bir Uzak Masaüstü Protokolü (. rdp) dosyası alır.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-108">The **Get-AzRemoteDesktopFile** cmdlet gets a Remote Desktop Protocol (.rdp) file.</span></span>

## <span data-ttu-id="6c9e5-109">ÖRNEKLERDEN</span><span class="sxs-lookup"><span data-stu-id="6c9e5-109">EXAMPLES</span></span>

### <span data-ttu-id="6c9e5-110">Örnek 1: uzak masaüstü dosyası alma</span><span class="sxs-lookup"><span data-stu-id="6c9e5-110">Example 1: Get a Remote Desktop file</span></span>
```
PS C:\> Get-AzRemoteDesktopFile -ResourceGroupName "ResourceGroup11" -Name "VirtualMachine07" -LocalPath "D:\RemoteDesktopFile07.rdp"
```

<span data-ttu-id="6c9e5-111">Bu komut, VirtualMachine07 adındaki sanal makine için Uzak Masaüstü dosyasını alır.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-111">This command gets the Remote Desktop file for the virtual machine named VirtualMachine07.</span></span>
<span data-ttu-id="6c9e5-112">Komut, sonucu D:\remotedesktopfile07.rdpadındaki dosyada depolar.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-112">The command stores the result in the file named D:\RemoteDesktopFile07.rdp.</span></span>

## <span data-ttu-id="6c9e5-113">PARAMETRELERINE</span><span class="sxs-lookup"><span data-stu-id="6c9e5-113">PARAMETERS</span></span>

### <span data-ttu-id="6c9e5-114">-DefaultProfile</span><span class="sxs-lookup"><span data-stu-id="6c9e5-114">-DefaultProfile</span></span>
<span data-ttu-id="6c9e5-115">Azure ile iletişim için kullanılan kimlik bilgileri, hesap, kiracı ve abonelik.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-115">The credentials, account, tenant, and subscription used for communication with azure.</span></span>

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

### <span data-ttu-id="6c9e5-116">-Başlat</span><span class="sxs-lookup"><span data-stu-id="6c9e5-116">-Launch</span></span>
<span data-ttu-id="6c9e5-117">Bu cmdlet. rdp dosyasını aldıktan sonra uzak masaüstünü başlatıyor.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-117">Indicates that this cmdlet launches Remote Desktop after it gets the .rdp file.</span></span>

```yaml
Type: System.Management.Automation.SwitchParameter
Parameter Sets: Launch
Aliases:

Required: True
Position: 3
Default value: None
Accept pipeline input: False
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e5-118">-LocalPath</span><span class="sxs-lookup"><span data-stu-id="6c9e5-118">-LocalPath</span></span>
<span data-ttu-id="6c9e5-119">Bu cmdlet. rdp dosyasını depolayan yerel tam yolu belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-119">Specifies the local full path where this cmdlet stores the .rdp file.</span></span>

```yaml
Type: System.String
Parameter Sets: Download
Aliases:

Required: True
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

```yaml
Type: System.String
Parameter Sets: Launch
Aliases:

Required: False
Position: 2
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e5-120">-Ad</span><span class="sxs-lookup"><span data-stu-id="6c9e5-120">-Name</span></span>
<span data-ttu-id="6c9e5-121">Bu cmdlet 'in aldığı kullanılabilirlik kümesinin adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-121">Specifies the name of the availability set that this cmdlet gets.</span></span>

```yaml
Type: System.String
Parameter Sets: (All)
Aliases: ResourceName, VMName

Required: True
Position: 1
Default value: None
Accept pipeline input: True (ByPropertyName)
Accept wildcard characters: False
```

### <span data-ttu-id="6c9e5-122">-ResourceGroupName</span><span class="sxs-lookup"><span data-stu-id="6c9e5-122">-ResourceGroupName</span></span>
<span data-ttu-id="6c9e5-123">Kaynak grubunun adını belirtir.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-123">Specifies the name of a resource group.</span></span>

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

### <span data-ttu-id="6c9e5-124">CommonParameters</span><span class="sxs-lookup"><span data-stu-id="6c9e5-124">CommonParameters</span></span>
<span data-ttu-id="6c9e5-125">Bu cmdlet ortak parametreleri destekler:-Debug,-ErrorAction,-ErrorVariable,-ınformationaction,-ınformationvariable,-OutVariable,-OutBuffer,-Pipelinedeğişken,-verbose,-WarningAction ve-Warningdeğişken.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-125">This cmdlet supports the common parameters: -Debug, -ErrorAction, -ErrorVariable, -InformationAction, -InformationVariable, -OutVariable, -OutBuffer, -PipelineVariable, -Verbose, -WarningAction, and -WarningVariable.</span></span> <span data-ttu-id="6c9e5-126">Daha fazla bilgi için [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216)bakın.</span><span class="sxs-lookup"><span data-stu-id="6c9e5-126">For more information, see [about_CommonParameters](https://go.microsoft.com/fwlink/?LinkID=113216).</span></span>

## <span data-ttu-id="6c9e5-127">GÖLGELENDIRICI</span><span class="sxs-lookup"><span data-stu-id="6c9e5-127">INPUTS</span></span>

### <span data-ttu-id="6c9e5-128">System. String</span><span class="sxs-lookup"><span data-stu-id="6c9e5-128">System.String</span></span>

## <span data-ttu-id="6c9e5-129">ÇıKıŞLAR</span><span class="sxs-lookup"><span data-stu-id="6c9e5-129">OUTPUTS</span></span>

### <span data-ttu-id="6c9e5-130">System. void</span><span class="sxs-lookup"><span data-stu-id="6c9e5-130">System.Void</span></span>

## <span data-ttu-id="6c9e5-131">NOTLARıNDA</span><span class="sxs-lookup"><span data-stu-id="6c9e5-131">NOTES</span></span>

## <span data-ttu-id="6c9e5-132">ILGILI BAĞLANTıLAR</span><span class="sxs-lookup"><span data-stu-id="6c9e5-132">RELATED LINKS</span></span>
